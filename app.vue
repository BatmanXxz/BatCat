<template>
  <div>
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
  </div>
</template>
<style>
body{
  font-size: 12px;
  margin: 0;
  padding: 0;
  ul li {
    list-style: none;
    margin: 0;
    padding: 0;
  }
}
.content{
  width: 1200px;
  height: 100%;
  margin: 0 auto;
}
.line-1{
  display: -webkit-box;
    -webkit-box-orient: vertical;
    text-overflow: ellipsis;
   /*  -webkit-line-clamp: 1; */
    overflow: hidden;
}
a:link{
  text-decoration: none;
  color: #333;
}
</style>