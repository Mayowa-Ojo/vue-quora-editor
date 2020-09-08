<template>
   <div id="app" class="pt-10">
      <div class="container mx-auto w-1/2">
         <Editor :toolbarId="generateId()"/>
         <Editor :toolbarId="generateId()"/>
      </div>
   </div>
</template>

<script>
   import Editor from "./components/Editor.vue";
   import shortid from "shortid";

   export default {
      name: "App",
      components: {
         Editor,
      },
      methods: {
         generateId: () => shortid.generate()
      }
   };
</script>

