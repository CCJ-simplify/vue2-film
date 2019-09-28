<template>
	<div class="footer">
		<mu-container>
			<mu-bottom-nav 
				:value.sync="shift"
				shift color="#e54847">
		    <mu-bottom-nav-item :value="1" title="电影" icon="theaters"></mu-bottom-nav-item>
		    <mu-bottom-nav-item :value="2" title="影院" icon="live_tv"></mu-bottom-nav-item>
		    <mu-bottom-nav-item :value="3" title="我的" icon="person"></mu-bottom-nav-item>
		  </mu-bottom-nav>
		</mu-container>
	</div>
</template>

<script>
	export default {
		name: 'BottomNav',
		data () {
		    return {
		      shift: 1
		    }
		 },
		computed: {
			NavSelect() {
				return this.$route.path
			}
		},
		methods:{
			
		}
	}
</script>

<style scoped>
    .footer {
		position: fixed;
		left: 0;
		bottom: 0;
		right: 0;
        width: 100%;
        height: 56px;
        z-index: 10;
		font-size: 30px;
    }
	.footer >>> .container {
		padding: 0rem;
		width: 100%;
        max-width: 100%;
    }
</style>