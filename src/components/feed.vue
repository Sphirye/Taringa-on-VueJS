<template>
	<body>
		<div class="cl_mainContainer">
			<div class="cl_feed">
				<div class="cl_postTitle">
					{{post.title}}
				</div>

				<div class="cl_postInfo">
					{{
						post.dDate + " " +
						post.mDate + " " +
						post.yDate + " " +
						post.rating
					}}
				</div>

				<div class="cl_postContent">
					{{
						post.content
					}}
				</div>
				
			</div>
			<div class="cl_tredings"></div>
		</div>
	</body>
</template>

<script>
export default {
	data() {
	    return {
	    	post: {
		    	title: '¿Como hacer nachos caseros? (Doritos)',
		    	user: '@Juanito777',
		    	dDate: '12',
		    	mDate: 'Mar',
		    	yDate: '2012',
		    	rating: '1447',
		    	content:'WEON SOY CURIFEO'
		    }
	    }
	}
}
</script>

<style>
.cl_mainContainer{
	display: flex;
	justify-content: center;
	border: 1px solid black;
	width: 100%;
	height: 100%;
}

.cl_mainContainer *{
	margin: 10px;
}

.cl_feed{
	border: 1px solid blue;
	width: 600px;
	min-height: 100px;
}

.cl_tredings{
	border: 1px solid yellow;
	width: 400px;
	min-height: 100px;
}

</style>