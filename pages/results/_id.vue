<template>
<div>
<h1>hello from results route {{$route.params.id}}</h1>
{{albumData}}
</div>
</template>
<script>
import axios from 'axios';
export default{
asyncData{{params}}{

	return axios.get('https://www.apple.com/search?term=${params.id}&entity=album')
	.then((response) => {
		return {albumData: response.data.results}
	});	
}
	middleware : 'search'

}

</script>