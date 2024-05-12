<script setup>
const route  = useRoute();
const { data } = await useFetch('/api/ticker/?id=' + route.params.id);
const coin = data.value[0];
</script>

<template>
    <main>
        <div>
            <h1>{{ coin.name }}</h1>
            <p>{{ coin.symbol }}</p>
            <p>{{ coin.rank }}</p>
            <p>{{ coin.price_usd }}</p>
            <p>{{ coin.market_cap_usd }}</p>
        </div>
    </main>
</template>