<script>
    async function getData() {
        let url = "https://api.open-meteo.com/v1/forecast?latitude=-42&longitude=174&hourly=temperature_2m&timezone=auto";
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
        console.log(data.hourly.temperature_2m);
        let day1 = 0;
        let day2 = 0;
        let day3 = 0;
        let day4 = 0;
        let day5 = 0;
        let day6 = 0;
        let day7 = 0;
        for (let i = 0; i < data.hourly.temperature_2m.length; i++){
            if (i < 24){
                day1 += data.hourly.temperature_2m[i];
            } else if (i < 48) {
                day2 += data.hourly.temperature_2m[i];
            } else if (i < 72) {
                day3 += data.hourly.temperature_2m[i];
            } else if (i < 96) {
                day4 += data.hourly.temperature_2m[i];
            } else if (i < 120) {
                day5 += data.hourly.temperature_2m[i];
            } else if (i < 144) {
                day6 += data.hourly.temperature_2m[i];
            } else if (i < 168) {
                day7 += data.hourly.temperature_2m[i];
            }
        }
        let sevenTemps = new Array(day1 / 24, day2 / 24, day3 / 24, day4 / 24, day5 / 24, day6 / 24, day7 / 24);
        //console.log(sevenTemps);
    }
    getData();
</script>

<style>

</style>