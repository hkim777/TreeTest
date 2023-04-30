<template>
  <input v-model="searchText" type="text" />
  <Tree
    :nodes="data"
    :search-text="searchText"
    :use-checkbox="true"
    :use-icon="true"
    use-row-delete
    show-child-count
    @nodeExpanded="onNodeExpanded"
    @update="onUpdate"
  />
</template>

<script>
import { ref } from "vue";
import Tree from "vue3-tree";
import "vue3-tree/dist/style.css";

export default {
  components: {
    Tree,
  },
  setup() {
    const data = ref([
      {
        id: 1,
        label: "力麗集團",
        nodes: [
          {
            id: 2,
            label: "總管理部",
            nodes: [
              {
                id: 3,
                label: "行政",
                nodes: [
                  {
                    id: 39,
                    label: "總務處",
                    nodes: [],
                  },
                  {
                    id: 65,
                    label: "採購處",
                    nodes: [],
                  },
                  {
                    id: 80,
                    label: "不動產開發處",
                    nodes: [],
                  },
                ],
              },
              {
                id: 17,
                label: "企劃",
                nodes: [
                  {
                    id: 18,
                    label: "稽核室",
                    nodes: [],
                  },
                  {
                    id: 36,
                    label: "法務室",
                    nodes: [],
                  },
                  {
                    id: 75,
                    label: "企劃處",
                    nodes: [],
                  },
                ],
              },
              {
                id: 212,
                label: "彰化廠務",
                nodes: [
                  {
                    id: 213,
                    label: "資財處",
                    nodes: [
                      {
                        id: 214,
                        label: "資財課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 215,
                    label: "假撚公用處",
                    nodes: [
                      {
                        id: 242,
                        label: "公用課",
                        nodes: [
                          {
                            id: 243,
                            label: "機械組",
                            nodes: [],
                          },
                          {
                            id: 350,
                            label: "電氣組",
                            nodes: [],
                          },
                          {
                            id: 434,
                            label: "儀電組",
                            nodes: [],
                          },
                          {
                            id: 439,
                            label: "公用組",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 229,
                    label: "廠務儲運處",
                    nodes: [
                      {
                        id: 230,
                        label: "假撚倉管二課",
                        nodes: [],
                      },
                      {
                        id: 238,
                        label: "廠務課",
                        nodes: [
                          {
                            id: 252,
                            label: "警衛",
                            nodes: [
                              {
                                id: 253,
                                label: "力鵬紡織",
                                nodes: [],
                              },
                              {
                                id: 310,
                                label: "力麗假撚",
                                nodes: [],
                              },
                              {
                                id: 311,
                                label: "尼龍二區",
                                nodes: [],
                              },
                              {
                                id: 436,
                                label: "力麗化纖",
                                nodes: [],
                              },
                              {
                                id: 443,
                                label: "力鵬尼龍",
                                nodes: [],
                              },
                              {
                                id: 459,
                                label: "尼龍倉儲區",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 261,
                            label: "環保",
                            nodes: [
                              {
                                id: 262,
                                label: "力鵬紡織",
                                nodes: [],
                              },
                              {
                                id: 329,
                                label: "力麗假撚",
                                nodes: [],
                              },
                              {
                                id: 448,
                                label: "力麗化纖",
                                nodes: [],
                              },
                              {
                                id: 454,
                                label: "力鵬尼龍",
                                nodes: [],
                              },
                              {
                                id: 495,
                                label: "力麟科技",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 274,
                            label: "舍監",
                            nodes: [
                              {
                                id: 275,
                                label: "力麗假撚",
                                nodes: [],
                              },
                              {
                                id: 484,
                                label: "力鵬尼龍",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 358,
                            label: "ISO文管中心",
                            nodes: [],
                          },
                          {
                            id: 429,
                            label: "力鵬尼龍棧板回收組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 244,
                        label: "假撚倉管一課",
                        nodes: [],
                      },
                      {
                        id: 251,
                        label: "尼龍倉管課",
                        nodes: [],
                      },
                      {
                        id: 315,
                        label: "化纖倉管課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 286,
                    label: "人資處",
                    nodes: [
                      {
                        id: 287,
                        label: "人事課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 305,
                    label: "化纖公用處",
                    nodes: [
                      {
                        id: 306,
                        label: "公用課",
                        nodes: [
                          {
                            id: 307,
                            label: "公用組",
                            nodes: [
                              {
                                id: 308,
                                label: "丙班",
                                nodes: [],
                              },
                              {
                                id: 326,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 347,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 357,
                                label: "乙班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 345,
                            label: "保養組",
                            nodes: [],
                          },
                          {
                            id: 451,
                            label: "汽電組",
                            nodes: [
                              {
                                id: 452,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 475,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 493,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 497,
                                label: "丙班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 314,
                    label: "尼龍公用處",
                    nodes: [
                      {
                        id: 355,
                        label: "公用課",
                        nodes: [
                          {
                            id: 356,
                            label: "保養組",
                            nodes: [],
                          },
                          {
                            id: 393,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 394,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 397,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 428,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 431,
                                label: "B班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 353,
                    label: "紡織公用處",
                    nodes: [
                      {
                        id: 354,
                        label: "公用課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 365,
                    label: "能源處",
                    nodes: [
                      {
                        id: 366,
                        label: "能源課",
                        nodes: [
                          {
                            id: 367,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 368,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 369,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 445,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 482,
                                label: "C班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 433,
                    label: "環安處",
                    nodes: [
                      {
                        id: 479,
                        label: "環安課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 506,
                    label: "廠務處",
                    nodes: [
                      {
                        id: 507,
                        label: "廠務課",
                        nodes: [
                          {
                            id: 508,
                            label: "環保",
                            nodes: [
                              {
                                id: 509,
                                label: "力鵬尼龍",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                ],
              },
            ],
          },
          {
            id: 24,
            label: "人力資源部",
            nodes: [],
          },
          {
            id: 30,
            label: "會計部",
            nodes: [
              {
                id: 31,
                label: "峰儀",
                nodes: [],
              },
              {
                id: 47,
                label: "力鵬",
                nodes: [],
              },
              {
                id: 58,
                label: "力麗",
                nodes: [],
              },
              {
                id: 71,
                label: "力麟",
                nodes: [],
              },
              {
                id: 74,
                label: "股務",
                nodes: [],
              },
            ],
          },
          {
            id: 33,
            label: "財務部",
            nodes: [
              {
                id: 34,
                label: "力鵬",
                nodes: [],
              },
              {
                id: 40,
                label: "力麗",
                nodes: [],
              },
            ],
          },
          {
            id: 46,
            label: "祕書處",
            nodes: [],
          },
          {
            id: 82,
            label: "研發中心",
            nodes: [
              {
                id: 83,
                label: "行銷企劃部",
                nodes: [
                  {
                    id: 84,
                    label: "客戶服務組",
                    nodes: [],
                  },
                ],
              },
            ],
          },
          {
            id: 309,
            label: "工程部",
            nodes: [],
          },
        ],
      },
      {
        id: 4,
        label: "力鵬企業股份有限公司",
        nodes: [
          {
            id: 5,
            label: "高端織品事業",
            nodes: [
              {
                id: 6,
                label: "業務部",
                nodes: [
                  {
                    id: 7,
                    label: "營管課",
                    nodes: [],
                  },
                  {
                    id: 19,
                    label: "採購生管處",
                    nodes: [],
                  },
                  {
                    id: 27,
                    label: "業務三處",
                    nodes: [],
                  },
                  {
                    id: 28,
                    label: "商品企劃處",
                    nodes: [
                      {
                        id: 29,
                        label: "印尼組",
                        nodes: [],
                      },
                      {
                        id: 45,
                        label: "樣品室",
                        nodes: [],
                      },
                      {
                        id: 100,
                        label: "家飾組",
                        nodes: [],
                      },
                      {
                        id: 102,
                        label: "企劃組",
                        nodes: [],
                      },
                      {
                        id: 113,
                        label: "品牌服務組",
                        nodes: [],
                      },
                      {
                        id: 116,
                        label: "針織組",
                        nodes: [],
                      },
                      {
                        id: 128,
                        label: "流行服飾組",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 35,
                    label: "業務二處",
                    nodes: [],
                  },
                  {
                    id: 37,
                    label: "業務五處",
                    nodes: [],
                  },
                  {
                    id: 41,
                    label: "業務六處",
                    nodes: [],
                  },
                  {
                    id: 44,
                    label: "船務課",
                    nodes: [],
                  },
                  {
                    id: 50,
                    label: "業務一處",
                    nodes: [],
                  },
                  {
                    id: 70,
                    label: "受染業務處",
                    nodes: [],
                  },
                  {
                    id: 72,
                    label: "託工處",
                    nodes: [],
                  },
                ],
              },
            ],
          },
          {
            id: 20,
            label: "尼龍事業",
            nodes: [
              {
                id: 21,
                label: "工塑業務部",
                nodes: [
                  {
                    id: 22,
                    label: "進出口業務處",
                    nodes: [],
                  },
                  {
                    id: 38,
                    label: "塑化業務處",
                    nodes: [],
                  },
                  {
                    id: 59,
                    label: "原料業務處",
                    nodes: [],
                  },
                ],
              },
              {
                id: 60,
                label: "業務部",
                nodes: [
                  {
                    id: 61,
                    label: "尼龍業務處",
                    nodes: [],
                  },
                  {
                    id: 69,
                    label: "上海力寶龍",
                    nodes: [],
                  },
                ],
              },
              {
                id: 264,
                label: "尼龍總廠",
                nodes: [
                  {
                    id: 265,
                    label: "技術處",
                    nodes: [
                      {
                        id: 266,
                        label: "包檢課",
                        nodes: [
                          {
                            id: 402,
                            label: "成檢組",
                            nodes: [
                              {
                                id: 403,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 406,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 407,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 432,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 472,
                                label: "A班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 411,
                            label: "包檢組",
                            nodes: [
                              {
                                id: 412,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 485,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 490,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 491,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 502,
                                label: "B班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 391,
                        label: "研設課",
                        nodes: [],
                      },
                      {
                        id: 456,
                        label: "化檢課",
                        nodes: [
                          {
                            id: 457,
                            label: "日班",
                            nodes: [],
                          },
                          {
                            id: 460,
                            label: "D班",
                            nodes: [],
                          },
                          {
                            id: 461,
                            label: "A班",
                            nodes: [],
                          },
                          {
                            id: 462,
                            label: "C班",
                            nodes: [],
                          },
                          {
                            id: 476,
                            label: "B班",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 294,
                    label: "聚一廠",
                    nodes: [
                      {
                        id: 295,
                        label: "聚一課",
                        nodes: [
                          {
                            id: 296,
                            label: "D班",
                            nodes: [],
                          },
                          {
                            id: 373,
                            label: "日班",
                            nodes: [],
                          },
                          {
                            id: 422,
                            label: "B班",
                            nodes: [],
                          },
                          {
                            id: 455,
                            label: "A班",
                            nodes: [],
                          },
                          {
                            id: 458,
                            label: "C班",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 327,
                    label: "總廠長室",
                    nodes: [
                      {
                        id: 328,
                        label: "生管課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 335,
                    label: "工務處",
                    nodes: [
                      {
                        id: 414,
                        label: "保養二課",
                        nodes: [],
                      },
                      {
                        id: 463,
                        label: "保養一課",
                        nodes: [
                          {
                            id: 464,
                            label: "B班",
                            nodes: [],
                          },
                          {
                            id: 486,
                            label: "A班",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 372,
                    label: "紡一廠",
                    nodes: [
                      {
                        id: 382,
                        label: "紡一課",
                        nodes: [
                          {
                            id: 383,
                            label: "準備組",
                            nodes: [
                              {
                                id: 384,
                                label: "紡口室",
                                nodes: [],
                              },
                              {
                                id: 410,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 435,
                                label: "WIPING",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 398,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 399,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 400,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 413,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 427,
                                label: "C班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 377,
                    label: "電儀處",
                    nodes: [
                      {
                        id: 385,
                        label: "電儀一課",
                        nodes: [
                          {
                            id: 386,
                            label: "A班",
                            nodes: [],
                          },
                          {
                            id: 468,
                            label: "B班",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 420,
                        label: "電儀二課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 416,
                    label: "聚二廠",
                    nodes: [
                      {
                        id: 417,
                        label: "聚二課",
                        nodes: [
                          {
                            id: 418,
                            label: "日班",
                            nodes: [],
                          },
                          {
                            id: 437,
                            label: "A班",
                            nodes: [],
                          },
                          {
                            id: 465,
                            label: "B班",
                            nodes: [],
                          },
                          {
                            id: 466,
                            label: "C班",
                            nodes: [],
                          },
                          {
                            id: 469,
                            label: "D班",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 421,
                    label: "工塑母粒專案組",
                    nodes: [
                      {
                        id: 480,
                        label: "日班",
                        nodes: [],
                      },
                    ],
                  },
                ],
              },
            ],
          },
          {
            id: 104,
            label: "染紗事業",
            nodes: [
              {
                id: 105,
                label: "業務部",
                nodes: [
                  {
                    id: 106,
                    label: "染紗業務處",
                    nodes: [],
                  },
                ],
              },
            ],
          },
          {
            id: 130,
            label: "平織事業",
            nodes: [
              {
                id: 131,
                label: "楊梅廠區",
                nodes: [
                  {
                    id: 132,
                    label: "織布廠",
                    nodes: [
                      {
                        id: 133,
                        label: "資源課",
                        nodes: [
                          {
                            id: 134,
                            label: "倉管組",
                            nodes: [],
                          },
                          {
                            id: 189,
                            label: "請購組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 135,
                        label: "織廠長室",
                        nodes: [],
                      },
                      {
                        id: 152,
                        label: "織造課",
                        nodes: [
                          {
                            id: 153,
                            label: "保全組",
                            nodes: [],
                          },
                          {
                            id: 154,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 155,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 159,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 161,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 172,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 192,
                                label: "E班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 157,
                        label: "準備課",
                        nodes: [
                          {
                            id: 158,
                            label: "整備組",
                            nodes: [],
                          },
                          {
                            id: 169,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 170,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 173,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 175,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 184,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 201,
                                label: "E班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 182,
                        label: "品管課",
                        nodes: [
                          {
                            id: 183,
                            label: "檢驗組",
                            nodes: [],
                          },
                          {
                            id: 209,
                            label: "製程組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 191,
                        label: "織研課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 136,
                    label: "生管處",
                    nodes: [],
                  },
                  {
                    id: 137,
                    label: "技術處",
                    nodes: [],
                  },
                  {
                    id: 138,
                    label: "整理處",
                    nodes: [
                      {
                        id: 139,
                        label: "整二課",
                        nodes: [
                          {
                            id: 140,
                            label: "整理組",
                            nodes: [
                              {
                                id: 141,
                                label: "B組",
                                nodes: [],
                              },
                              {
                                id: 176,
                                label: "A組",
                                nodes: [],
                              },
                              {
                                id: 198,
                                label: "C組",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 181,
                            label: "定型組",
                            nodes: [
                              {
                                id: 185,
                                label: "A組",
                                nodes: [],
                              },
                              {
                                id: 187,
                                label: "C組",
                                nodes: [],
                              },
                              {
                                id: 190,
                                label: "B組",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 197,
                        label: "整一課",
                        nodes: [
                          {
                            id: 204,
                            label: "整理組",
                            nodes: [
                              {
                                id: 205,
                                label: "C組",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 211,
                            label: "定型組",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 142,
                    label: "研發處",
                    nodes: [
                      {
                        id: 143,
                        label: "染研課",
                        nodes: [],
                      },
                      {
                        id: 160,
                        label: "研發室",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 144,
                    label: "染二廠",
                    nodes: [
                      {
                        id: 145,
                        label: "染二廠長室",
                        nodes: [],
                      },
                      {
                        id: 146,
                        label: "染二課",
                        nodes: [
                          {
                            id: 177,
                            label: "準備組",
                            nodes: [
                              {
                                id: 178,
                                label: "A組",
                                nodes: [],
                              },
                              {
                                id: 195,
                                label: "E組",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 179,
                            label: "染色組",
                            nodes: [
                              {
                                id: 180,
                                label: "A組",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 164,
                        label: "品二課",
                        nodes: [
                          {
                            id: 165,
                            label: "品檢組",
                            nodes: [
                              {
                                id: 166,
                                label: "A組",
                                nodes: [],
                              },
                              {
                                id: 188,
                                label: "B組",
                                nodes: [],
                              },
                              {
                                id: 196,
                                label: "E組",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 147,
                    label: "廠務處",
                    nodes: [
                      {
                        id: 148,
                        label: "總廠長室",
                        nodes: [],
                      },
                      {
                        id: 162,
                        label: "廠務課",
                        nodes: [
                          {
                            id: 163,
                            label: "廠務組",
                            nodes: [],
                          },
                          {
                            id: 186,
                            label: "資財組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 171,
                        label: "託管課",
                        nodes: [],
                      },
                      {
                        id: 199,
                        label: "工安室",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 149,
                    label: "染一廠",
                    nodes: [
                      {
                        id: 150,
                        label: "染一課",
                        nodes: [
                          {
                            id: 151,
                            label: "染色組",
                            nodes: [],
                          },
                          {
                            id: 206,
                            label: "準備組",
                            nodes: [
                              {
                                id: 207,
                                label: "E組",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 193,
                        label: "品一課",
                        nodes: [
                          {
                            id: 194,
                            label: "品檢組",
                            nodes: [
                              {
                                id: 200,
                                label: "E組",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 202,
                        label: "紗檢課",
                        nodes: [],
                      },
                      {
                        id: 203,
                        label: "染一廠長室",
                        nodes: [],
                      },
                      {
                        id: 208,
                        label: "染紗課",
                        nodes: [
                          {
                            id: 210,
                            label: "E組",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 156,
                    label: "工務處",
                    nodes: [],
                  },
                  {
                    id: 167,
                    label: "公用處",
                    nodes: [
                      {
                        id: 168,
                        label: "原動課",
                        nodes: [],
                      },
                      {
                        id: 174,
                        label: "環工課",
                        nodes: [],
                      },
                    ],
                  },
                ],
              },
              {
                id: 235,
                label: "彰化廠區",
                nodes: [
                  {
                    id: 236,
                    label: "彰化紡織廠",
                    nodes: [
                      {
                        id: 237,
                        label: "織造課",
                        nodes: [
                          {
                            id: 263,
                            label: "日班",
                            nodes: [],
                          },
                          {
                            id: 278,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 279,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 280,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 292,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 319,
                                label: "C班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 477,
                            label: "保全組",
                            nodes: [],
                          },
                          {
                            id: 492,
                            label: "製程組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 245,
                        label: "撚絲課",
                        nodes: [
                          {
                            id: 246,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 247,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 255,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 446,
                                label: "C班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 257,
                            label: "製程組",
                            nodes: [],
                          },
                          {
                            id: 473,
                            label: "保全組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 248,
                        label: "準備課",
                        nodes: [
                          {
                            id: 249,
                            label: "運轉一區",
                            nodes: [
                              {
                                id: 250,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 254,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 256,
                                label: "穿綜組",
                                nodes: [],
                              },
                              {
                                id: 304,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 352,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 438,
                                label: "日班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 288,
                            label: "運轉二區",
                            nodes: [
                              {
                                id: 289,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 299,
                                label: "D班",
                                nodes: [],
                              },
                              {
                                id: 388,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 450,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 467,
                                label: "B班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 283,
                        label: "品管課",
                        nodes: [],
                      },
                      {
                        id: 290,
                        label: "生管課",
                        nodes: [
                          {
                            id: 291,
                            label: "倉管組",
                            nodes: [],
                          },
                          {
                            id: 426,
                            label: "管制組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 293,
                        label: "廠長室",
                        nodes: [],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        ],
      },
      {
        id: 8,
        label: "力傑能源股份有限公司",
        nodes: [],
      },
      {
        id: 9,
        label: "力麗企業股份有限公司",
        nodes: [
          {
            id: 14,
            label: "聚酯事業一",
            nodes: [
              {
                id: 15,
                label: "業務部",
                nodes: [
                  {
                    id: 16,
                    label: "內銷業務處",
                    nodes: [],
                  },
                  {
                    id: 23,
                    label: "外銷業務處",
                    nodes: [],
                  },
                  {
                    id: 73,
                    label: "電子材料處",
                    nodes: [],
                  },
                  {
                    id: 103,
                    label: "商品企劃處",
                    nodes: [],
                  },
                ],
              },
              {
                id: 126,
                label: "中壢廠區",
                nodes: [],
              },
            ],
          },
          {
            id: 57,
            label: "總經理室",
            nodes: [],
          },
          {
            id: 216,
            label: "聚酯事業二",
            nodes: [
              {
                id: 217,
                label: "假撚總廠",
                nodes: [
                  {
                    id: 218,
                    label: "技術處",
                    nodes: [
                      {
                        id: 219,
                        label: "包檢一課",
                        nodes: [
                          {
                            id: 239,
                            label: "品檢組",
                            nodes: [],
                          },
                          {
                            id: 240,
                            label: "包檢組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 221,
                        label: "包檢二課",
                        nodes: [
                          {
                            id: 222,
                            label: "包檢組",
                            nodes: [
                              {
                                id: 223,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 302,
                                label: "乙班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 297,
                        label: "品管課",
                        nodes: [
                          {
                            id: 298,
                            label: "一區",
                            nodes: [],
                          },
                          {
                            id: 364,
                            label: "二區",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 220,
                    label: "工務處",
                    nodes: [
                      {
                        id: 276,
                        label: "工務二課",
                        nodes: [
                          {
                            id: 277,
                            label: "保養組",
                            nodes: [],
                          },
                          {
                            id: 313,
                            label: "專區組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 284,
                        label: "工務一課",
                        nodes: [
                          {
                            id: 285,
                            label: "專區組",
                            nodes: [],
                          },
                          {
                            id: 376,
                            label: "保養組",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 224,
                    label: "假撚一廠",
                    nodes: [
                      {
                        id: 225,
                        label: "撚絲一課",
                        nodes: [
                          {
                            id: 226,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 227,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 233,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 234,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 282,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 351,
                                label: "丙班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 267,
                        label: "撚絲二課",
                        nodes: [
                          {
                            id: 268,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 269,
                                label: "丙班",
                                nodes: [],
                              },
                              {
                                id: 272,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 300,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 312,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 324,
                                label: "丁班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 228,
                    label: "生管處",
                    nodes: [
                      {
                        id: 241,
                        label: "生管課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 231,
                    label: "研設處",
                    nodes: [
                      {
                        id: 232,
                        label: "開發組",
                        nodes: [],
                      },
                      {
                        id: 346,
                        label: "售服組",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 258,
                    label: "假撚二廠",
                    nodes: [
                      {
                        id: 259,
                        label: "包檢課",
                        nodes: [
                          {
                            id: 260,
                            label: "包檢組",
                            nodes: [],
                          },
                          {
                            id: 379,
                            label: "品檢組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 273,
                        label: "品管課",
                        nodes: [],
                      },
                      {
                        id: 361,
                        label: "撚絲課",
                        nodes: [
                          {
                            id: 362,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 363,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 378,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 381,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 440,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 444,
                                label: "丙班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 370,
                        label: "工務課",
                        nodes: [
                          {
                            id: 371,
                            label: "專區組",
                            nodes: [],
                          },
                          {
                            id: 449,
                            label: "保養組",
                            nodes: [],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 387,
                    label: "總廠長室",
                    nodes: [],
                  },
                ],
              },
              {
                id: 270,
                label: "化纖總廠",
                nodes: [
                  {
                    id: 271,
                    label: "紡一廠",
                    nodes: [
                      {
                        id: 316,
                        label: "紡一課",
                        nodes: [
                          {
                            id: 317,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 318,
                                label: "丙班",
                                nodes: [],
                              },
                              {
                                id: 375,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 395,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 453,
                                label: "乙班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 321,
                            label: "準備組",
                            nodes: [
                              {
                                id: 322,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 401,
                                label: "WIPING",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 281,
                    label: "技術處",
                    nodes: [
                      {
                        id: 334,
                        label: "包檢課",
                        nodes: [
                          {
                            id: 359,
                            label: "物檢室",
                            nodes: [
                              {
                                id: 360,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 430,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 474,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 501,
                                label: "丙班",
                                nodes: [],
                              },
                              {
                                id: 504,
                                label: "丁班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 374,
                            label: "包裝日班",
                            nodes: [],
                          },
                          {
                            id: 389,
                            label: "運轉組",
                            nodes: [
                              {
                                id: 390,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 396,
                                label: "丙班",
                                nodes: [],
                              },
                              {
                                id: 405,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 447,
                                label: "乙班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 408,
                            label: "化檢室",
                            nodes: [
                              {
                                id: 409,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 481,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 483,
                                label: "日班",
                                nodes: [],
                              },
                              {
                                id: 489,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 496,
                                label: "丙班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 301,
                    label: "總廠長室",
                    nodes: [],
                  },
                  {
                    id: 303,
                    label: "研設處",
                    nodes: [],
                  },
                  {
                    id: 320,
                    label: "電儀處",
                    nodes: [
                      {
                        id: 323,
                        label: "電儀一課",
                        nodes: [],
                      },
                      {
                        id: 325,
                        label: "電儀二課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 330,
                    label: "聚一廠",
                    nodes: [
                      {
                        id: 331,
                        label: "聚一課",
                        nodes: [
                          {
                            id: 332,
                            label: "製程組",
                            nodes: [
                              {
                                id: 333,
                                label: "甲班",
                                nodes: [],
                              },
                              {
                                id: 344,
                                label: "丁班",
                                nodes: [],
                              },
                              {
                                id: 392,
                                label: "乙班",
                                nodes: [],
                              },
                              {
                                id: 415,
                                label: "丙班",
                                nodes: [],
                              },
                            ],
                          },
                          {
                            id: 342,
                            label: "配包組",
                            nodes: [
                              {
                                id: 343,
                                label: "粒包",
                                nodes: [],
                              },
                              {
                                id: 380,
                                label: "配製",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                    ],
                  },
                  {
                    id: 341,
                    label: "回收造粒廠",
                    nodes: [
                      {
                        id: 404,
                        label: "造粒課",
                        nodes: [],
                      },
                    ],
                  },
                  {
                    id: 348,
                    label: "工務處",
                    nodes: [
                      {
                        id: 349,
                        label: "紡保課",
                        nodes: [],
                      },
                      {
                        id: 419,
                        label: "聚保課",
                        nodes: [],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        ],
      },
      {
        id: 10,
        label: "力麗科技股份有限公司",
        nodes: [
          {
            id: 12,
            label: "軟體服務事業部",
            nodes: [
              {
                id: 13,
                label: "企業e化事業處",
                nodes: [],
              },
              {
                id: 48,
                label: "專案辦公室",
                nodes: [],
              },
              {
                id: 49,
                label: "資訊服務事業處",
                nodes: [],
              },
              {
                id: 53,
                label: "台北事業處",
                nodes: [],
              },
              {
                id: 68,
                label: "高檢事業處",
                nodes: [],
              },
              {
                id: 81,
                label: "台中事業處",
                nodes: [],
              },
              {
                id: 114,
                label: "軟體研發辦公室",
                nodes: [],
              },
            ],
          },
          {
            id: 32,
            label: "行政部",
            nodes: [],
          },
          {
            id: 52,
            label: "總經理室",
            nodes: [
              {
                id: 66,
                label: "會計",
                nodes: [],
              },
            ],
          },
          {
            id: 54,
            label: "系統服務部",
            nodes: [
              {
                id: 55,
                label: "台北",
                nodes: [
                  {
                    id: 56,
                    label: "業務支援處",
                    nodes: [],
                  },
                  {
                    id: 64,
                    label: "業務一處",
                    nodes: [],
                  },
                  {
                    id: 94,
                    label: "業務二處",
                    nodes: [],
                  },
                  {
                    id: 98,
                    label: "業務三處",
                    nodes: [],
                  },
                  {
                    id: 115,
                    label: "原委會專案業務處",
                    nodes: [],
                  },
                  {
                    id: 120,
                    label: "業務六處",
                    nodes: [],
                  },
                ],
              },
            ],
          },
          {
            id: 62,
            label: "經銷服務事業部",
            nodes: [
              {
                id: 63,
                label: "技術支援處",
                nodes: [],
              },
              {
                id: 67,
                label: "台中辦事處",
                nodes: [],
              },
              {
                id: 76,
                label: "產品行銷處",
                nodes: [],
              },
              {
                id: 77,
                label: "高雄業務處",
                nodes: [],
              },
              {
                id: 85,
                label: "台北業務三處",
                nodes: [],
              },
              {
                id: 91,
                label: "台北業務二處",
                nodes: [],
              },
              {
                id: 95,
                label: "台北業務六處",
                nodes: [],
              },
              {
                id: 97,
                label: "台北業務一處",
                nodes: [],
              },
              {
                id: 99,
                label: "台北業務七處",
                nodes: [],
              },
              {
                id: 101,
                label: "台北業務五處",
                nodes: [],
              },
            ],
          },
        ],
      },
      {
        id: 11,
        label: "力麟科技股份有限公司",
        nodes: [
          {
            id: 336,
            label: "薄膜事業",
            nodes: [
              {
                id: 337,
                label: "彰化廠區",
                nodes: [
                  {
                    id: 338,
                    label: "彰化廠",
                    nodes: [
                      {
                        id: 339,
                        label: "機電課",
                        nodes: [
                          {
                            id: 340,
                            label: "機械公用組",
                            nodes: [],
                          },
                          {
                            id: 494,
                            label: "電儀組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 423,
                        label: "裁包課",
                        nodes: [
                          {
                            id: 424,
                            label: "裁包組",
                            nodes: [
                              {
                                id: 425,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 478,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 500,
                                label: "A班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 441,
                        label: "生產課",
                        nodes: [
                          {
                            id: 442,
                            label: "製程組",
                            nodes: [
                              {
                                id: 498,
                                label: "C班",
                                nodes: [],
                              },
                              {
                                id: 499,
                                label: "B班",
                                nodes: [],
                              },
                              {
                                id: 503,
                                label: "A班",
                                nodes: [],
                              },
                              {
                                id: 515,
                                label: "D班",
                                nodes: [],
                              },
                            ],
                          },
                        ],
                      },
                      {
                        id: 470,
                        label: "廠長室",
                        nodes: [
                          {
                            id: 471,
                            label: "倉管組",
                            nodes: [],
                          },
                          {
                            id: 514,
                            label: "生管組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 487,
                        label: "技術課",
                        nodes: [
                          {
                            id: 488,
                            label: "檢驗組",
                            nodes: [],
                          },
                        ],
                      },
                      {
                        id: 505,
                        label: "研設課",
                        nodes: [],
                      },
                    ],
                  },
                ],
              },
            ],
          },
        ],
      },
      {
        id: 25,
        label: "印尼力寳龍公司",
        nodes: [
          {
            id: 26,
            label: "業務部",
            nodes: [],
          },
          {
            id: 86,
            label: "生產部",
            nodes: [
              {
                id: 129,
                label: "行政處",
                nodes: [],
              },
            ],
          },
        ],
      },
      {
        id: 42,
        label: "力寶龍企業股份有限公司",
        nodes: [
          {
            id: 43,
            label: "商品處",
            nodes: [],
          },
          {
            id: 78,
            label: "財會處",
            nodes: [],
          },
          {
            id: 87,
            label: "營運處",
            nodes: [
              {
                id: 88,
                label: "新莊店",
                nodes: [],
              },
              {
                id: 89,
                label: "吉林店",
                nodes: [],
              },
              {
                id: 92,
                label: "義大店",
                nodes: [],
              },
              {
                id: 93,
                label: "師大店",
                nodes: [],
              },
              {
                id: 96,
                label: "信義店",
                nodes: [],
              },
            ],
          },
          {
            id: 118,
            label: "電子商務處",
            nodes: [],
          },
          {
            id: 119,
            label: "營運處(經銷)",
            nodes: [],
          },
        ],
      },
      {
        id: 51,
        label: "峰儀科技股份有限公司",
        nodes: [
          {
            id: 107,
            label: "系統工程處",
            nodes: [],
          },
          {
            id: 108,
            label: "業務一處",
            nodes: [],
          },
          {
            id: 109,
            label: "網路工程處",
            nodes: [],
          },
          {
            id: 110,
            label: "業務二處",
            nodes: [],
          },
          {
            id: 111,
            label: "業務三處",
            nodes: [],
          },
          {
            id: 112,
            label: "業務支援處",
            nodes: [],
          },
          {
            id: 117,
            label: "行政處",
            nodes: [],
          },
          {
            id: 121,
            label: "區域事業處",
            nodes: [
              {
                id: 122,
                label: "網路",
                nodes: [
                  {
                    id: 123,
                    label: "台中",
                    nodes: [],
                  },
                  {
                    id: 127,
                    label: "高雄",
                    nodes: [],
                  },
                ],
              },
              {
                id: 124,
                label: "業務",
                nodes: [
                  {
                    id: 125,
                    label: "高雄",
                    nodes: [],
                  },
                ],
              },
            ],
          },
        ],
      },
      {
        id: 79,
        label: "凱祥投資股份有限公司",
        nodes: [],
      },
      {
        id: 90,
        label: "伊德石化股份有限公司",
        nodes: [],
      },
      {
        id: 510,
        label: "力寳龍能源股份有限公司",
        nodes: [
          {
            id: 511,
            label: "綠能事業",
            nodes: [
              {
                id: 512,
                label: "彰化廠區",
                nodes: [
                  {
                    id: 513,
                    label: "綠能發展處",
                    nodes: [],
                  },
                ],
              },
            ],
          },
        ],
      },
    ]);
    const searchText = ref("");
    const onNodeExpanded = (node, state) => {
      console.log("state: ", state);
      console.log("node: ", node);
    };

    const onUpdate = (nodes) => {
      console.log("nodes:", nodes);
    };

    return {
      data,
      searchText,
      onNodeExpanded,
      onUpdate,
    };
  },
};
</script>

<style lang="scss">
</style>