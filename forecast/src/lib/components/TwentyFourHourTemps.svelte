<script>
    async function getData() {
        let url = "https://api.open-meteo.com/v1/forecast?latitude=-42&longitude=174&hourly=temperature_2m&timezone=auto&forecast_days=1";
        try {
        const response = await fetch(url);
        if (!response.ok) {
            throw new Error(`Response status: ${response.status}`);
        }
        const data = await response.json();
        temp(data);
        } catch (error) {
        console.error(error.message);
        }
    }
    function temp(data) {
        //console.log(data.hourly.temperature_2m);
    }
    getData();
</script>

<style>

</style>