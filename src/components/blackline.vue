<template>
    <div class="card">
<div class="card-header text-left">
<p id="nazivbl"><b>Blackline</b></p>
</div>
<div class="card-body p-0">
<img id="blackline" class="card-img-top" src="@/assets/blackline.jpg"/>
</div>
<div class="card-footer text-muted text-left">
    <router-link id="lk" to="/opisline">About the species</router-link>
</div>
</div>
</template>

<script>
export default{
 name: 'blackline',
};
</script>

<style lang="scss">
#blackline{
    height:300px;
    width: 350px;
}
#nazivbl{
    margin:5px;
    color:rgb(93, 92, 165);
    font-size:20px;
}
#lk{
    color:rgb(93, 92, 165);
}

</style>