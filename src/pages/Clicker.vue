<template>
    <div class="columns">
        <div class="column is-one-third has-text-centered">
            <b>{{clicks}} clicks</b>  
            <br>
            <b>{{cps}} ~CLICKS PER SECOND~</b>  
            <img @click="clickClick()" :class="{'click': clickClass}" src="https://static.vecteezy.com/system/resources/previews/008/506/564/original/watermelon-split-cartoon-png.png">   
        </div>
        <div class="columnC">
            <button @click="upgrade(0.1, 10)" class="button is-white" :disabled="clicks<10">Osta 0.1 klikke sekundis 10 kliki eest</button>     
            <br>
            <br>
            <button @click="upgradeA(1, 100)" class="button is-white" :disabled="clicks<100">Osta 1 klikke sekundis 100 kliki eest</button> 
            <br>
            <br>
            <button @click="upgradeB(10, 1000)" class="button is-white" :disabled="clicks<1000">Osta 10 klikke sekundis 1000 kliki eest</button>
            <br>  
            <br>    
            <button @click="upgradeC(100, 10000)" class="button is-white" :disabled="clicks<10000">Osta 100 klikke sekundis 10000 kliki eest</button> 
            <br>
            <br>
            <button @click="upgradeD(1000, 100000)" class="button is-white" :disabled="clicks<100000">Osta 1000 klikke sekundis 100000 kliki eest</button> 
            <br>
            <br>
            <button @click="upgradeE(10000, 1000000)" class="button is-white" :disabled="clicks<1000000">Osta 10000 klikke sekundis 1000000 kliki eest</button> 
            <br>
            <br>
            <button @click="upgradeF(100000, 10000000)" class="button is-white" :disabled="clicks<10000000">Osta 100000 klikke sekundis 10000000 kliki eest</button> 
            <br>
            <br>
            <button @click="upgradeG(1000000, 100000000)" class="button is-white" :disabled="clicks<100000000">Osta 1000000 klikke sekundis 100000000 kliki eest</button> 
            <br>
            <br>
            <button @click="upgrade1(50, 0)" class="button is-primary" :disabled="clicks<0">Võta pangast klikki laenu</button> 

        </div>
    </div>


</template>

<script>
export default {
    created(){
        setInterval(()=>{
            this.clicks += this.cps;
            this.clicks = parseFloat(this.clicks.toFixed(1));
        }, 1000);

    },
    data(){
        return {
            clickClass: false,
            clicks: 0,
            cps: 0
        }
    },
        computed:{
        displayastros(){
            return parseFloat(this.astros.toFixed(1));
        },
        displayCps(){
            return parseFloat(this.cps.toFixed(1));
    },
},
    methods: {
        clickClick(){
            this.clicks++;
            this.clickClass = true;
            setTimeout(()=> {
                this.clickClass = false;
            }, 100);
        },
        upgrade(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 0.1 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                upgradeA(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 1 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                upgradeB(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 10 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                upgradeC(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 100 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                upgradeD(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 1000 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                upgradeE(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 10000 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                pgradeF(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 100000 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
                        pgradeF(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`PALJU ÕNNE SAAD NÜÜD 1000000 KLIKKI SEKUNDIS JUURDE!`);
            }
        },
        upgrade1(cps, cost){
            if(this.clicks >= cost){
                this.clicks -= cost;
                this.cps += cps;
                alert(`VÕTSID 50 KLIKKI SEKUNDIS LAENU PANGAST`);
            }
        }
    }
}


    

</script>

<style scoped>

    .button{
    color: rgb(14, 14, 122);
    background-color: aqua;
    font-family: fantasy;
    border-radius: 15%;
    
    }
    .columnC {
        position: absolute;
        right: 90%;
        top: 160px;
    
    
    }
    .img {
        position: absolute;
        top:50%;
    }

    img.click {
        transform: scale(1.5);
        transition: 0.5s;
    }
    b {
        color: white;
    }

</style>
