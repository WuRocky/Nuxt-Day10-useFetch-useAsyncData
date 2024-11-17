<script setup>
// // 1. 有提供 key 就可以使用 refreshNuxtData() 資料發更新
// const userData = ref({});
// const { data } = await useAsyncData("getRandomuser1", () =>
//   $fetch("https://randomuser.me/api/")
// );

// // 透過  refreshNuxtData() 請求 API
// const refresh = () => {
//   refreshNuxtData("getRandomuser1");
// }

// // 2. 用 transform 函式修改&nbsp;handler&nbsp;請求的結果
// const { data: userTransformData } = await useAsyncData(
//   "getRandomuser2",
//   () => $fetch("https://randomuser.me/api/"),
//   {
//     transform: (response) => {
//       // 修改 response 的結果，取出並回傳物件結構
//       const [resultObject] = response.results;
      
//       // 一定要 return 資料，否則在 userTransformData 會取不到資料 
//       return resultObject;
//     },
//   }
// );

// // 3. 用 pick 參數從 handler 函式回傳的資料中，從物件取出 info 屬性的資料
// const { data: userPickData } = await useAsyncData(
//   "getRandomuser3",
//   () =>
//     $fetch("https://randomuser.me/api/", {
//       query: {
//         seed: "be579ffd62ede3ce",
//       },
//     }),
//   { pick: ["info"] }
// );
</script>

<template>
  <h1>首頁頁面</h1>
  <!-- <div>
    <hr />
    <h2>使用 key 搭配 refreshNuxtData() 觸發資料更新</h2>
    <img
      :src="data.results[0].picture?.large"
      :alt="`${data.results[0].name?.first} ${data.results[0].name?.last}`"
    />
    <h1>{{ data.results[0].name?.first }} {{ data.results[0].name?.last }}</h1>
    <h3>Email: {{ data.results[0].email }}</h3>

    <button @click="refresh">更新資料</button>
  </div> -->

  <!-- <div>
    <h2>用 transform 函式修改&nbsp;handler&nbsp;請求的結果</h2>
    <img
      :src="userTransformData.picture?.large"
      :alt="`${userTransformData.name?.first} ${userTransformData.name?.last}`"
    />
    <h1>
      {{ userTransformData.name?.first }} {{ userTransformData.name?.last }}
    </h1>
    <h3>Email: {{ userTransformData.email }}</h3>
    
    <hr />
  </div> -->

  <!-- <div>
    <pre>
    {{ userPickData }}
    </pre>
  </div> -->
</template>

<style 
>
</style>
