<template>
<div>
<h1>hello from results route {{$route.params.id}}</h1>
{{$store.albums}}
</div>
</template>
<script>
export default{
	middleware : 'search'
}
</script>