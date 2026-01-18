<script lang="ts">
    import gsap from "gsap";
    import { onMount } from "svelte";

    let Head1,Head2,Test1,Test2,Button1:any;
    let timline = gsap.timeline();
    onMount(()=> 
    timline.from(Head1,{ x: -1000, duration: 0.25}).from(Head2,{ x: -1000, duration:0.25}).from(Test1,{x: -1000,duration:0.25}).from(Test2, {x:-1000, duration:0.25}));
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