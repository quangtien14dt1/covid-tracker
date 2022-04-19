<template>

</template>
<script>
export default {
    setup() {
        const loading = ref(true)
        const title = ref('Global')
        const dataDate = ref('')
        const status = ref('{}')
        const countries = ref([])

        const fetchCovidData = async () => {
            const res = await fetch('https://api.covid19api.com/summary')
            return await res.json()
        }

        const getCountryData = (country) => {
            status.value = country
            title.value = country.Country
        }


    },
}
</script>
