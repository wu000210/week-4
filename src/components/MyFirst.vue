<template>
<div>
<h2>Hello{{ name}}!
</h2>
<ul>
 <li>Age: {{ age }}</li>
 <li>Color: {{ color }}</li>
 <li>{{ treat }}</li>
</ul>

</div>
</template>
<script>
export default {
    props: ["treat"],
    data: function() {
        return {
            name:"MyFirst",
            age: 6,
            color: "pink"
        };
    }
};
</script>
<style>
h2 {
    color: coral;
}
</style>