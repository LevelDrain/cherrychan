<template>
    <div class="container">
        <div class="menu">
            <table>
                <tr>
                    <th>装備品</th>
                    <th>お金（ルピー）</th>
                    <th>購入済</th>
                </tr>
                <tr v-for="tool in tools" :key="tool.id">
                    <td>{{tool.item}}</td>
                    <td>{{tool.money}}</td>
                    <td><input type="checkbox" :checked="tool.check" @change="changeState(tool)"/></td>
                </tr>
                <tr>
                    <td>{{sendData}}</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                tools: [
                    {id: 1, item: "古代兵装・兜", money: 2000, check: false},
                    {id: 2, item: "古代兵装・上鎧", money: 2000, check: true},
                    {id: 3, item: "古代兵装・下鎧", money: 2000, check: false}
                ],
                sendData: [],
            }
        },
        watch: {
            tools: {
                handler: function () {
                    this.sendData = this.tools
                    console.log('変更')
                },
                deep: true
            }
        },
        methods: {
            changeState(tool) {
                tool.check = !tool.check
            },
            postData() {
                //axiosでapiに送信する想定
                this.sendData.push({id: this.tools.id, check: this.tools.check})
                let jsonSendData = JSON.parse(JSON.stringify(this.sendData))
                jsonSendData.forEach(element => {
                    console.log(element)
                })
                //console.log(jsonSendData)
            }
        }
    };
</script>

<style></style>
