<template>
        <dd-chart :datasets="datasets" :labels="labels" :width="width" :height="height" >
    </dd-chart>
 </template> 

<script>
    import DdChart from './component/ddChart'

        export default {
            data: function() {
                return {
                    width: 500,
                    height: 200,
                    labels: ['1月', '2月', '3月', '4月', '5月', '6月'],
                    datasets: [{
                        label: '数据一',
                        data: [110, 90, 100, 81, 106, 75, 88]
                    }, {
                        label: '数据二',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    }, {
                        label: '数据三',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    },{
                        label: '数据四',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    }, {
                        label: '数据五',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    }, {
                        label: '数据六',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    }, {
                        label: '数据七',
                        data: [90, 70, 80, 60, 55, 33, 44]
                    }]
                }
            },
            components: {
                DdChart,
            }
        }

</script>
