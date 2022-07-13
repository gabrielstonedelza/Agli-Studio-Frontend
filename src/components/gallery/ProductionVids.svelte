<script context="module">
	export async function load({ fetch }) {
		const prductionVideos = await fetch(`http://127.0.0.1:8000/pro_vids/`, {
			headers: {
				'content-type': 'application/json',
				accept: 'application/json'
			}
		});
		const proVids = await prductionVideos.json();
		console.log(proVids);

		if (prductionVideos.ok) {
			return {
				props: {
					proVids
				}
			};
		}
	}
	
</script>