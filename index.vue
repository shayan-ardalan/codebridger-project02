
<template>
  <div>
    <h1>قیمت‌های</h1>

   <div v-if="pending">در حال بارگذاری...</div>
    
 <div v-else-if="error">خطا در دریافت اطلاعات</div>
    
   <div v-else class="prices-grid">
   <PriceCard
     v-for="coin in data"
   :key="coin.symbol"
    v-bind="coin"
      />
    </div>
  </div>
</template>

<script setup>

const { data, pending, error } = await useFetch('/api/prices')


useHead({
  title: 'قیمت‌های  ارزهای دیجیتال'
})
</script>

<style scoped>
.prices-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  padding: 1rem;
}
</style> 