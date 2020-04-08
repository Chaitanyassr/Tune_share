<template>
<div>
<h1>hello from results route {{$route.params.id}}</h1>
{{$store.state.albums}}
</div>
</template>
<script>
export default{
asyncData{{params}}{

	
}
	middleware : 'search'

}

</script>