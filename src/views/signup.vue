<template>
    <div class="about">
    <div class="container">
    <div class="row">
    <div class="col-sm"></div>
    <div class="col-sm">
    <br/>

    <form>
    <div class="form-group">
    <p id="admin"><b>Sign-up</b></p>
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" v-model="username" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email" />
    <p id="mail">We'll never share you e-mail with anyone else.</p>
    </div>

    <div id="loz" class="form-group">
    <label for="exampleInputPassword2">Password</label>
    <br/>
    <input type="password" v-model="password" class="form-control" id="exampleInputPassword1" placeholder="Password" />
    </div>

    <div id="loz" class="form-group">
    <label for="exampleInputPassword2">Repeat password</label>
    <br/>
    <input type="password" v-model="passwordRepeat" class="form-control" id="exampleInputPassword2" placeholder="Password" /><br/>
    </div>
 
    <button type="button" @click="signup()" class="btn btn-secondary">Submit</button>
    <br/>
    
    </form>
    </div>
    <div class="col-sm"></div>
    </div>
    </div>
    </div>
    </template>

<script>
import store from "@/store";
import {firebase} from "@/firebase";
import router from "@/router";

    export default {
        name: "signup",
        data() {
            return {
                username:"",
                password:"",
                passwordRepeat:"",
                
            };
        },
    methods:{
        signup(){
            firebase
            .auth()
            .createUserWithEmailAndPassword(this.username, this.password)
            .then(
                    function(error){
                        console.log('uspješna registracija');
                    });

               },
            },
        };

</script>


<style lang="scss">
#admin{
    font-size:30px;
    color:rgb(93, 92, 165);
}
#loz{
    margin-top:10px;
}
#log{
    font-size:18px;
    color:rgb(66, 64, 64);
    margin-left:40%;
}
#pass,#mail{
    color:rgb(230, 54, 54);
    margin-bottom:0px;
}
</style>