<script lang="ts">
    import gsap from "gsap";
    import { onMount } from "svelte";

    let Head1,Head2,Test1,Test2,Button1:any;
    let timline = gsap.timeline();
    onMount(()=> 
    timline.from(Head1,{ x: -100, duration: 0.25, opacity:0}).from(Head2,{ x: -100,y:-50, duration:0.25, opacity:0}).from(Test1,{x: -100,duration:0.25,y:-50, opacity:0}).from(Test2, {x:-100,y:-50, duration:0.25, opacity:0}));
</script>
<svelte:head>
    <title>
        Test 
    </title>
</svelte:head>
<h1 bind:this={Head1}>Name</h1>
<input bind:this={Test1} type="text" value="Name">
<br>
<h1 bind:this={Head2}>Surname</h1>
<input bind:this={Test2} type="text" value="Surname">
<br>
<h1>
<button>Submit</button></h1>