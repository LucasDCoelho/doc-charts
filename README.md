# Documentação de todos os gráficos da ATBI-SEFAZ

## Descrição

Este documento descreve a configuração de gráficos instruidos para ATBI-SEFAZ. Guia é baseado no Figma, https://www.figma.com/design/KFRRjH0WUrKp8QxWicmrwG/SEFAZ?node-id=2-374&t=iTcyjozemBbM1ne8-1

## Configuração dos Gráficos

### DADOS DE PESAGEM:

#### Número de Passagens X Equipamento

```javascript
option = {
  title: {
    text: 'Número de Passagens X Equipamento'
  },
  tooltip: {
    trigger: 'axis',
    axisPointer: {
      type: 'shadow'
    }
  },
  legend: {},
  grid: {
    left: '3%',
    right: '4%',
    bottom: '3%',
    containLabel: true
  },
  yAxis: {
    type: 'value',
    boundaryGap: [0, 0.01]
  },
  xAxis: {
    type: 'category',
    data: ['Jun/2023', 'Jul/2023', 'Ago/2023', 'Set/2023', 'Out/2023', 'Nov/2023', 'Dez/2023', 'Jan/2024', 'Fev/2024', 'Mar/2024', 'Abr/2024', 'Mai/2024']
  },
  series: [
    {
      name: 'Caminhão',
      type: 'bar',
      data: [18203, 23489, 29034, 104970, 131744, 630230,181654,48468,468412,418413,8742,456846]
    },
    {
      name: 'Veículos Diversos',
      type: 'bar',
      data: [19325, 23438, 31000, 121594, 134141, 681807,84168,41612,168476,6451,441238,86746]
    }
  ]
};
```

### Números de alertas
```javascript
option = {
  xAxis: {
    type: 'category',
    data: ['Jun/2023', 'Jul/2023', 'Ago/2023', 'Set/2023', 'Out/2023', 'Nov/2023', 'Dez/2023', 'Jan/2024', 'Fev/2024', 'Mar/2024', 'Abr/2024', 'Mai/2024']
  },
  yAxis: {
    type: 'value'
  },
  series: [
    {
      data: [320, 330, 390, 191, 301, 302, 320, 230, 220, 234,334 ,191, 212, 232],
      type: 'bar'
    }
  ]
};
```

#### Número de alertas X Equipamento
```javascript
option = {
    title: {
        text: 'Gráfico de Barras com Segmentos Mensais'
    },
    tooltip: {
        trigger: 'axis',
        axisPointer: {
            type: 'shadow'
        }
    },
    legend: {
        data: ['Jun/2023', 'Jul/2023', 'Ago/2023', 'Set/2023', 'Out/2023', 'Nov/2023', 'Dez/2023', 'Jan/2024', 'Fev/2024', 'Mar/2024', 'Abr/2024', 'Mai/2024']
    },
    grid: {
        left: '3%',
        right: '4%',
        bottom: '3%',
        containLabel: true
    },
    xAxis: {
        type: 'value'
    },
    yAxis: {
        type: 'category',
        data: ['ATB5007', 'ATB5006', 'ATB5005', 'ATB5004', 'ATB5003', 'ATB5002', 'ATB5001']
    },
    series: [
        {
            name: 'Jun/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Jul/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Ago/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Set/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Out/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Nov/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Dez/2023',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        },
        {
            name: 'Jan/2024',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [320, 330, 390, 334, 301, 302, 320]
        },
        {
            name: 'Fev/2024',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [210, 230, 220, 234, 191, 212, 232]
        },
        {
            name: 'Mar/2024',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [310, 330, 290, 334, 201, 232, 205]
        },
        {
            name: 'Abr/2024',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [410, 330, 190, 454, 291, 282, 80]
        },
        {
            name: 'Mai/2024',
            type: 'bar',
            stack: 'total',
            label: {
                show: true
            },
            data: [1320, 1330, 1290, 934, 901, 832, 820]
        }
    ]
};
```
__________________________________________

## FISCALIZAÇÃO

#### Quantidade de passagens X Alertas X Equipamento

```javascript
myChart.showLoading();
$.get(
  ROOT_PATH + '/data/asset/data/obama_budget_proposal_2012.list.json',
  function (obama_budget_2012) {
    myChart.hideLoading();
    option = {
      tooltip: {
        trigger: 'axis',
        axisPointer: {
          type: 'shadow',
          label: {
            show: true
          }
        }
      },
      toolbox: {
        show: true,
        feature: {
          mark: { show: true },
          dataView: { show: true, readOnly: false },
          magicType: { show: true, type: ['line', 'bar'] },
          restore: { show: true },
          saveAsImage: { show: true }
        }
      },
      calculable: true,
      legend: {
        data: ['Growth', 'Passagens', 'Alertas'],
        itemGap: 5
      },
      grid: {
        top: '12%',
        left: '1%',
        right: '10%',
        containLabel: true
      },
      xAxis: [
        {
          type: 'category',
          data: ["ATB0008", "ATB0020", "ATB0080",  "ATB00086", "ATB0200", "ATB0322", "ATB0423", "ATB0541", "ATB0123"]
        }
      ],
      yAxis: [
        {
          type: 'value',
          name: 'Quantidade',
          axisLabel: {
            formatter: function (a) {
              a = +a;
              return isFinite(a) ? echarts.format.addCommas(+a / 1000) : '';
            }
          }
        }
      ],
      dataZoom: [
        {
          show: true,
          start: 94,
          end: 100
        },
        {
          type: 'inside',
          start: 94,
          end: 100
        },
        {
          show: true,
          yAxisIndex: 0,
          filterMode: 'empty',
          width: 30,
          height: '80%',
          showDataShadow: false,
          left: '93%'
        }
      ],
      series: [
        {
          name: 'Passagens',
          type: 'bar',
          data: [1452, 2681, 2108, 987, 2764, 1445, 2049, 1882, 2987, 1502, 345, 2469]
        },
        {
          name: 'Alertas',
          type: 'bar',
          data: [2098, 567, 1480, 2999, 1724, 1855, 2346, 1457, 2561, 1983, 2765, 995]
        }
      ]
    };
    myChart.setOption(option);
  }
);
```
_______

## ALERTAS

#### Número de Alertas e Tipos X Período
```javascript
 // Dados de exemplo preenchendo todos os dias de 6 a 5 e todas as categorias
    var data = [
     // INTERNAÇÃO DE MERCADORIA
    [6, 0, 2], [7, 0, 11], [8, 0, 13], [9, 0, 3], [10, 0, 8], [11, 0, 15], [12, 0, 4], [13, 0, 10], [14, 0, 6], [15, 0, 7], [16, 0, 2], [17, 0, 10], [18, 0, 5], [19, 0, 4], [20, 0, 1], [21, 0, 9], [22, 0, 6], [23, 0, 1], [0, 0, 9], [1, 0, 3], [2, 0, 8], [3, 0, 5], [4, 0, 12], [5, 0, 2],
    // VEÍCULO FORA DE ROTA
    [6, 1, 3], [7, 1, 12], [8, 1, 10], [9, 1, 5], [10, 1, 9], [11, 1, 14], [12, 1, 10], [13, 1, 5], [14, 1, 8], [15, 1, 2], [16, 1, 3], [17, 1, 11], [18, 1, 8], [19, 1, 7], [20, 1, 4], [21, 1, 12], [22, 1, 6], [23, 1, 1], [0, 1, 14], [1, 1, 6], [2, 1, 11], [3, 1, 13], [4, 1, 7], [5, 1, 3],
    // DÉBITO DE IPVA
    [6, 2, 7], [7, 2, 11], [8, 2, 9], [9, 2, 6], [10, 2, 11], [11, 2, 9], [12, 2, 8], [13, 2, 14], [14, 2, 5], [15, 2, 10], [16, 2, 6], [17, 2, 8], [18, 2, 7], [19, 2, 4], [20, 2, 5], [21, 2, 13], [22, 2, 6], [23, 2, 13], [0, 2, 12], [1, 2, 5], [2, 2, 4], [3, 2, 10], [4, 2, 14], [5, 2, 7],
    // EXCESSO DE PBT
    [6, 3, 4], [7, 3, 9], [8, 3, 11], [9, 3, 6], [10, 3, 5], [11, 3, 8], [12, 3, 7], [13, 3, 8], [14, 3, 9], [15, 3, 4], [16, 3, 6], [17, 3, 8], [18, 3, 7], [19, 3, 9], [20, 3, 5], [21, 3, 10], [22, 3, 6], [23, 3, 2], [0, 3, 3], [1, 3, 5], [2, 3, 7], [3, 3, 8], [4, 3, 1], [5, 3, 4],
    // CARGA MAIOR QUE CAPACIDADE
    [6, 4, 1], [7, 4, 9], [8, 4, 10], [9, 4, 7], [10, 4, 5], [11, 4, 8], [12, 4, 9], [13, 4, 7], [14, 4, 6], [15, 4, 5], [16, 4, 8], [17, 4, 7], [18, 4, 5], [19, 4, 9], [20, 4, 11], [21, 4, 12], [22, 4, 6], [23, 4, 8], [0, 4, 5], [1, 4, 11], [2, 4, 13], [3, 4, 2], [4, 4, 4], [5, 4, 1],
    // VEÍCULO SEM MDFE
    [6, 5, 10], [7, 5, 8], [8, 5, 6], [9, 5, 7], [10, 5, 8], [11, 5, 12], [12, 5, 14], [13, 5, 9], [14, 5, 10], [15, 5, 6], [16, 5, 8], [17, 5, 12], [18, 5, 15], [19, 5, 3], [20, 5, 11], [21, 5, 5], [22, 5, 6], [23, 5, 7], [0, 5, 7], [1, 5, 7], [2, 5, 12], [3, 5, 11], [4, 5, 14], [5, 5, 9]
    ];

    var option = {
      tooltip: {
        position: 'top'
      },
      animation: true,
      grid: {
        height: '50%',
        top: '10%'
      },
      xAxis: {
        type: 'category',
        data: Array.from({ length: 24 }, (_, i) => ((i + 6) % 24).toString().padStart(2, '0')),
        splitArea: {
          show: true
        }
      },
      yAxis: {
        type: 'category',
        data: ['INTERNAÇÃO DE MERCADORIA', 'VEÍCULO FORA DE ROTA', 'DÉBITO DE IPVA', 'EXCESSO DE PBT', 'CARGA MAIOR QUE CAPACIDADE', 'VEÍCULO SEM MDFE'],
        splitArea: {
          show: true
        }
      },
      visualMap: {
        min: 0,
        max: 15,
        calculable: true,
        orient: 'horizontal',
        left: 'center',
        bottom: '15%'
      },
      series: [{
        name: 'Infrações',
        type: 'heatmap',
        data: data,
        label: {
          show: true
        },
        emphasis: {
          itemStyle: {
            shadowBlur: 10,
            shadowColor: 'rgba(0, 0, 0, 0.5)'
          }
        }
      }]
    };
```

#### Quantidade de alertas X Tipo
```javascript
option = {
  tooltip: {
    trigger: 'axis',
    axisPointer: {
      type: 'cross',
      crossStyle: {
        color: '#999'
      }
    }
  },
  toolbox: {
    feature: {
      dataView: { show: true, readOnly: false },
      magicType: { show: true, type: ['line', 'bar'] },
      restore: { show: true },
      saveAsImage: { show: true }
    }
  },
  legend: {
    data: ['Passagens', 'Alertas']
  },
  xAxis: [
    {
      type: 'category',
      data: [
      "Veículo Sem MDFE", 
      "Carga Medida Maior que MDFE", 
      "Veículo Fora de Rota",  
      "Internação de Mercadoria", 
      "Lista de Restrições"
      ],
      axisPointer: {
        type: 'shadow'
      },
      axisLabel:{
        fontSize: 10,
        interval: 0,
      },
      
    }
  ],
  yAxis: [
    {
      type: 'value',
      name: 'Passagens',
      min: 0,
      max: 5000,
      interval: 500,
    },
    {
      type: 'value',
      name: 'Alertas',
      min: 0,
      max: 5000,
      interval: 500,
    }
  ],
  series: [
    {
      name: 'Passagens',
      type: 'bar',
      tooltip: {
        valueFormatter: function (value) {
          return value;
        }
      },
      data:[2834, 1587, 492, 2248, 1675]
    },
    {
      name: 'Alertas',
      type: 'line',
      yAxisIndex: 1,
      tooltip: {
        valueFormatter: function (value) {
          return value;
        }
      },
      data:[2098, 567, 1480, 2999, 1724]
    }
  ]
};
```

#### Tipo de Alerta X Equipamento
```javascript
myChart.showLoading();
$.get(
  ROOT_PATH + '/data/asset/data/obama_budget_proposal_2012.list.json',
  function (obama_budget_2012) {
    myChart.hideLoading();
    option = {
      tooltip: {
        trigger: 'axis',
        axisPointer: {
          type: 'shadow',
          label: {
            show: true
          }
        }
      },
      toolbox: {
        show: true,
        feature: {
          mark: { show: true },
          dataView: { show: true, readOnly: false },
          magicType: { show: true, type: ['line', 'bar'] },
          restore: { show: true },
          saveAsImage: { show: true }
        }
      },
      calculable: true,
      legend: {
        data: ["Veículo Sem MDFE", "Carga Medida Maior que MDFE", "Excesso de PBT", "Veículo Fora de Rota", "Internação de Mercadoria"],
        itemGap: 15
      },
      grid: {
        top: '12%',
        left: '1%',
        right: '10%',
        containLabel: true
      },
      yAxis: [
        {
          type: 'category',
          data: ["ATB0008", "ATB0020", "ATB0080", "ATB00086", "ATB0200", "ATB0322", "ATB0423", "ATB0541", "ATB0123"]
        }
      ],
      xAxis: [
        {
          type: 'value',
          name: 'Quantidade',
          axisLabel: {
            formatter: function (a) {
              a = +a;
              return isFinite(a) ? echarts.format.addCommas(+a / 100) : '';
            }
          }
        }
      ],
      dataZoom: [
        {
          show: true,
          type: 'slider',
          orient: 'vertical',
          yAxisIndex: 0,
          start: 100,
          end: 0,
          height: '65%',
          width: 20,
          right: '5%'
        },
        {
          show: true,
          type: 'slider',
          orient: 'horizontal',
          xAxisIndex: 0,
          start: 0,
          end: 100,
          height: 20,
          bottom: '8%'
        }
      ],
      series: [
        {
          name: 'Veículo Sem MDFE',
          type: 'bar',
          data: [1375, 2889, 901, 2211, 1574, 309, 2931, 1756, 2184, 1640, 1972, 1822]
        },
        {
          name: 'Carga Medida Maior que MDFE',
          type: 'bar',
          data: [2098, 567, 1480, 2999, 1724, 1855, 2346, 1457, 2561, 1983, 2765, 995]
        },
        {
          name: 'Excesso de PBT',
          type: 'bar',
          data: [2834, 1587, 492, 2248, 1675, 2984, 957, 1620, 2541, 431, 2893, 1234]
        },
        {
          name: 'Veículo Fora de Rota',
          type: 'bar',
          data: [1452, 2681, 2108, 987, 2764, 1445, 2049, 1882, 2987, 1502, 345, 2469]
        },
        {
          name: 'Internação de Mercadoria',
          type: 'bar',
          data: [1375, 2889, 901, 2211, 1769, 309, 2931, 1756, 2184, 1640, 1972, 1822]
        }
      ]
    };
    myChart.setOption(option);
  }
);
```

____

## MDFE

#### Veículo sem mdfe
```javascript
option = {
  title: {
    text: 'Top 5 com Quantidade'
  },
  xAxis: {
    type: 'category',
    data: ["ABC1324", "ADC1464", "CDA1864", "CET1264", "AMW5464"]
  },
  yAxis: {
    type: 'value'
  },
  series: [
    {
      data: [120, 200, 150, 80, 70],
      type: 'bar'
    }
  ]
};
```

#### Carga medida maior que carga mdfe
```javascript
option = {
  title: {
    text: 'Gráfico de Barras Horizontais'
  },
  xAxis: {
    type: 'value'
  },
  yAxis: {
    type: 'category',
    data: ["ABC1324", "ADC1464", "CDA1864", "CET1264", "AMW5464"]
  },
  series: [
    {
      data: [120, 200, 150, 80, 70],
      type: 'bar'
    }
  ]
};
```

#### Excesso de PBT
```javascript
option = {
  tooltip: {
    trigger: 'item',
    formatter: '{a} <br/>{b}: {c} ({d}%)'
  },
  legend: {
    data: [
      'ABC1324',
      'ADC1464',
      'CDA1864',
      'CET1264',
      'AMW5464',
      'Category1',
      'Category2'
    ]
  },
  series: [
    {
      name: 'Main Categories',
      type: 'pie',
      selectedMode: 'single',
      radius: [0, '30%'],
      label: {
        position: 'inner',
        fontSize: 14
      },
      labelLine: {
        show: false
      },
      data: [
        { value: 1548, name: 'CDA1864', selected: true },
        { value: 679, name: 'ABC1324' },
        { value: 775, name: 'ADC1464' },
      ]
    },
    {
      name: 'Sub Categories',
      type: 'pie',
      radius: ['45%', '60%'],
      labelLine: {
        length: 30
      },
      label: {
        formatter: '{a|{a}}{abg|}\n{hr|}\n  {b|{b}：}{c}  {per|{d}%}  ',
        backgroundColor: '#F6F8FC',
        borderColor: '#8C8D8E',
        borderWidth: 1,
        borderRadius: 4,
        rich: {
          a: {
            color: '#6E7079',
            lineHeight: 22,
            align: 'center'
          },
          hr: {
            borderColor: '#8C8D8E',
            width: '100%',
            borderWidth: 1,
            height: 0
          },
          b: {
            color: '#4C5058',
            fontSize: 14,
            fontWeight: 'bold',
            lineHeight: 33
          },
          per: {
            color: '#fff',
            backgroundColor: '#4C5058',
            padding: [3, 4],
            borderRadius: 4
          }
        }
      },
      data: [
        { value: 1048, name: 'CDA1864' },
        { value: 335, name: 'ABC1324' },
        { value: 310, name: 'ADC1464' },
        { value: 251, name: 'CET1264' },
        { value: 234, name: 'AMW5464' },
      ]
    }
  ]
};
```

#### Veículo fora de rota
```javascript
option = {
  title: {
    text: 'Nightingale'
  },
  series: [
    {
      name: 'Nightingale',
      type: 'pie',
      radius: [30, 110],
      center: ['50%', '50%'],
      roseType: 'area',
      data: [
        {value: 10, name: 'ABC1324'},
        {value: 5, name: 'ADC1464'},
        {value: 15, name: 'CDA1864'},
        {value: 25, name: 'CET1264'},
        {value: 20, name: 'AMW5464'}
      ]
    }
  ]
};
```

#### Internação de mercadoria
```javascript
option = {
  title: {
    text: 'Treemap'
  },
  series: [
    {
      name: 'Treemap',
      type: 'treemap',
      data: [
        {
          name: 'ABC1324',
          value: 120
        },
        {
          name: 'ADC1464',
          value: 200
        },
        {
          name: 'CDA1864',
          value: 150
        },
        {
          name: 'CET1264',
          value: 80
        },
        {
          name: 'AMW5464',
          value: 70
        }
      ]
    }
  ]
};
```


