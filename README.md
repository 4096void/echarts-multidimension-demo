## echarts-multidimension-demo
> Just an npm archive of https://blog.csdn.net/mulumeng981/article/details/77848644 's sroucecode (⚠️ echarts fixed to 3.7.1 ⚠️)

```javascript
const MulDimensionChart = require('echarts-multidimension-demo');

// data sample
let data = [
  [
    "企业",
    "余姚站",
    "2013-05",
    0.015,
    800
  ],
  [
    "企业",
    "奉化站",
    "2013-07",
    0.0033,
    6500
  ],
  [
    "企业",
    "宁红站",
    "2013-09",
    0.02,
    200
  ],
  [
    "企业",
    "彩虹站",
    "2013-11",
    0.015,
    134
  ],
  [
    "企业",
    "慈城站",
    "2013-01",
    0.015,
    300
  ],
  [
    "企业",
    "春晓站",
    "2013-03",
    0.011,
    903
  ],
  [
    "普通客户",
    "余姚站",
    "2013-03",
    0.017,
    134
  ],
  [
    "普通客户",
    "奉化站",
    "2013-05",
    0.013,
    1250
  ],
  [
    "普通客户",
    "宁红站",
    "2013-07",
    0.017,
    903
  ],
  [
    "普通客户",
    "仓基站",
    "2013-01",
    0.019,
    903
  ]
];
var dimension = [{
    "key": "cust_type",
    "tagkey": "cust_type",
    "alias": "cust_type",
    "continuity": "00",
    "colType": "string"
  },
  {
    "key": "faxing_state",
    "tagkey": "faxing_state",
    "alias": "faxing_state",
    "continuity": "00",
    "colType": "string"
  },
  {
    "key": "Month",
    "tagkey": "Month",
    "alias": "Month",
    "originTag": "full_date",
    "timeFormat": "yyyy-mm",
    "continuity": "10",
    "colType": "date"
  }
];
var measure = [{
    "key": "huan_bi",
    "tagkey": "huan_bi",
    "alias": "总和_huan_bi",
    "prop": "sum",
    "continuity": "11",
    "colType": "float",
    "state": "bar"
  },
  {
    "key": "faxing_sum",
    "tagkey": "faxing_sum",
    "alias": "总和_faxing_sum",
    "prop": "sum",
    "continuity": "11",
    "colType": "float",
    "state": "bar"
  }
];

let chart = new MulDimensionChart(
  document.getElementByid('container'),
  data,
  dimension,
  measure,
);
```
