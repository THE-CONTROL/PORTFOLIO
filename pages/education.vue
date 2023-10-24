<template>
  <div class="w-full mt-16 sm:px-16 px-4 text-white">
    <h2 class="font-bold text-4xl">Education</h2>
    <div class="w-full overflow-auto">
        <table class="w-fit mx-auto text-center mt-4 bg-[#474747] rounded-lg">
            <thead class="w-fit border-b-2 border-[#252525]">
                <tr>
                    <th v-for="(item, index) in tableHeaders" :key="index" class="p-2">{{ item }}</th>
                </tr>
            </thead>
            <tbody v-for="(item, index) in tableData" :key="index"  class="w-fit">
                <tr>
                    <td class="p-4">{{ item.from }}</td>
                    <td class="p-4">{{ item.to }}</td>
                    <td class="p-4">{{ item.ins }}</td>
                    <td class="p-4">{{ item.cert }}</td>
                </tr>
            </tbody>
        </table>
    </div>
  </div>
</template>

<script>
export default {
    name: "EducationPage",
    setup() {
        const tableHeaders = [
            "From",
            "To",
            "Institution",
            "Certificate Obtained"
        ]
        const tableData = [
            {
                "from": "2004", 
                "to": "2013", 
                "ins": "Baptist Children Academy", 
                "cert": "Primary School Leaving Certificate"
            },
            {
                "from": "2013", 
                "to": "2019", 
                "ins": "Baptist High School", 
                "cert": "West African Senior School Certificate(WASSC)"
            },
            {
                "from": "2019", 
                "to": "Present", 
                "ins": "University of Benin", 
                "cert": "Bachelor of Medicine, Bachelor of Surgery(MBBS)"
            }
        ]

        return { tableHeaders, tableData }
    }
}
</script>

<style>

</style>