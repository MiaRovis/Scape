<template>
    <div class="card">
<div class="card-header text-left">
<p id="nazivdi"><b>Diamond</b></p>
</div>
<div class="card-body p-0">
<img id="diamond" class="card-img-top" src="@/assets/diamond.jpg"/>
</div>
<div class="card-footer text-muted text-left">
    <router-link id="lk" to="/opisdiamond">About the species</router-link>
</div>
</div>
</template>

<script>
export default{
 name: 'diamond',
};
</script>

<style lang="scss">
#diamond{
    height:300px;
    width: 350px;
}
#nazivdi{
    margin:5px;
    color:rgb(93, 92, 165);
    font-size:20px;
}
#lk{
    color:rgb(93, 92, 165);
}
</style>