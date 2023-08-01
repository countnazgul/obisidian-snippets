## Description

Get the UI structure of the app - list of the available sheets and their viz objects (with their type, position and size)

## Code

```javascript
const objProps = {
        "qInfo": {
          "qType": "SheetList",
          "qId": ""
        },
        "qAppObjectListDef": {
          "qData": {
            "title": "/qMetaDef/title",
            "labelExpression": "/labelExpression",
            "showCondition": "/showCondition",
            "description": "/qMetaDef/description",
            "descriptionExpression": "/qMetaDef/descriptionExpression",
            "thumbnail": "/qMetaDef/thumbnail",
            "cells": "/cells",
            "rank": "/rank",
            "columns": "/columns",
            "rows": "/rows"
          },
          "qType": "sheet"
        }
      };

const qObj = await app.createSessionObject(objProps);

const qObjLayout = await qObj.getLayout();
```

## Response structure (overall)

![[Pasted image 20230801101903.png]]

## Response structure (qAppObjectList overall)

![[Pasted image 20230801102100.png]]

## Response structure (qData.cells)

![[Pasted image 20230801102201.png]]

## Example response (full)

```javascript
{
  "qLayout": {
    "qInfo": {
      "qId": "3066378e-a183-43f4-83af-f9434f7300ae",
      "qType": "SheetList"
    },
    "qMeta": {
      "privileges": [
        "read",
        "update",
        "delete",
        "exportdata"
      ]
    },
    "qSelectionInfo": {},
    "qAppObjectList": {
      "qItems": [
        {
          "qInfo": {
            "qId": "DuXnF",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "Sales & Margin Analysis",
            "description": "View sales and margin data by state, region, and product."
          },
          "qData": {
            "rank": 1,
            "columns": 24,
            "rows": 12,
            "title": "Sales & Margin Analysis",
            "labelExpression": "",
            "showCondition": "",
            "description": "View sales and margin data by state, region, and product.",
            "descriptionExpression": "",
            "thumbnail": "",
            "cells": [
              {
                "name": "vCNaSe",
                "type": "map",
                "col": 0,
                "row": 0,
                "colspan": 14,
                "rowspan": 6
              },
              {
                "name": "akDGX",
                "type": "barchart",
                "col": 14,
                "row": 0,
                "colspan": 10,
                "rowspan": 6
              },
              {
                "name": "KnASd",
                "type": "table",
                "col": 14,
                "row": 6,
                "colspan": 10,
                "rowspan": 6
              },
              {
                "name": "BqZP",
                "type": "scatterplot",
                "col": 0,
                "row": 6,
                "colspan": 7,
                "rowspan": 3
              },
              {
                "name": "CLfuxL",
                "type": "scatterplot",
                "col": 7,
                "row": 6,
                "colspan": 7,
                "rowspan": 3
              },
              {
                "name": "KzjmJ",
                "type": "scatterplot",
                "col": 0,
                "row": 9,
                "colspan": 7,
                "rowspan": 3
              },
              {
                "name": "vvAbDn",
                "type": "scatterplot",
                "col": 7,
                "row": 9,
                "colspan": 7,
                "rowspan": 3
              }
            ]
          }
        },
        {
          "qInfo": {
            "qId": "JzJMza",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "KPI Dashboard",
            "description": "View Margin %, Sales, and Budget. Navigate o other sheets for KPI details."
          },
          "qData": {
            "rank": 0,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "NrHfp",
                "type": "kpi",
                "col": 0,
                "row": 0,
                "colspan": 7,
                "rowspan": 4
              },
              {
                "name": "ajMAEu",
                "type": "kpi",
                "col": 0,
                "row": 4,
                "colspan": 7,
                "rowspan": 4
              },
              {
                "name": "bJSZttJ",
                "type": "kpi",
                "col": 0,
                "row": 8,
                "colspan": 7,
                "rowspan": 4
              },
              {
                "name": "MEAjCJ",
                "type": "gauge",
                "col": 7,
                "row": 0,
                "colspan": 8,
                "rowspan": 4
              },
              {
                "name": "fNGRa",
                "type": "piechart",
                "col": 7,
                "row": 4,
                "colspan": 8,
                "rowspan": 4
              },
              {
                "name": "nPLRub",
                "type": "piechart",
                "col": 7,
                "row": 8,
                "colspan": 8,
                "rowspan": 4
              },
              {
                "name": "qamd",
                "type": "linechart",
                "col": 15,
                "row": 0,
                "colspan": 9,
                "rowspan": 4
              },
              {
                "name": "JcJvj",
                "type": "linechart",
                "col": 15,
                "row": 4,
                "colspan": 9,
                "rowspan": 4
              },
              {
                "name": "WJYuPN",
                "type": "linechart",
                "col": 15,
                "row": 8,
                "colspan": 9,
                "rowspan": 4
              }
            ],
            "title": "KPI Dashboard",
            "labelExpression": "",
            "showCondition": "",
            "description": "View Margin %, Sales, and Budget. Navigate o other sheets for KPI details.",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "LChBs",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "Sales Rep Performance",
            "description": "Analyze sales data for sales reps. Understand which reps are performing the best and the worst."
          },
          "qData": {
            "rank": 3,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "ufWRp",
                "type": "table",
                "col": 0,
                "row": 0,
                "colspan": 7,
                "rowspan": 7
              },
              {
                "name": "fQdkG",
                "type": "barchart",
                "col": 0,
                "row": 7,
                "colspan": 7,
                "rowspan": 5
              },
              {
                "name": "bsxkrg",
                "type": "scatterplot",
                "col": 7,
                "row": 0,
                "colspan": 9,
                "rowspan": 7
              },
              {
                "name": "pyQPxfg",
                "type": "scatterplot",
                "col": 7,
                "row": 7,
                "colspan": 9,
                "rowspan": 5
              },
              {
                "name": "savsPXN",
                "type": "treemap",
                "col": 16,
                "row": 0,
                "colspan": 8,
                "rowspan": 12
              }
            ],
            "title": "Sales Rep Performance",
            "labelExpression": "",
            "showCondition": "",
            "description": "Analyze sales data for sales reps. Understand which reps are performing the best and the worst.",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "jDSPJ",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "Sales Analysis",
            "description": "View sales by city, sales rep, and product."
          },
          "qData": {
            "rank": 2,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "dcksUYY",
                "type": "map",
                "col": 0,
                "row": 0,
                "colspan": 14,
                "rowspan": 6
              },
              {
                "name": "PyQXKt",
                "type": "barchart",
                "col": 0,
                "row": 6,
                "colspan": 7,
                "rowspan": 6
              },
              {
                "name": "MRmuW",
                "type": "barchart",
                "col": 7,
                "row": 6,
                "colspan": 7,
                "rowspan": 6
              },
              {
                "name": "RfEbJ",
                "type": "pivot-table",
                "col": 14,
                "row": 0,
                "colspan": 10,
                "rowspan": 12
              }
            ],
            "title": "Sales Analysis",
            "labelExpression": "",
            "showCondition": "",
            "description": "View sales by city, sales rep, and product.",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "GnAzpy",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "Budget Analysis",
            "description": "Analyze actual versus budget budget data. Is the company on target to hit its budgeted amounts?"
          },
          "qData": {
            "rank": 4,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "qEqbcMm",
                "type": "combochart",
                "col": 3,
                "row": 0,
                "colspan": 21,
                "rowspan": 4
              },
              {
                "name": "mHzvAm",
                "type": "filterpane",
                "col": 0,
                "row": 0,
                "colspan": 3,
                "rowspan": 8
              },
              {
                "name": "EzEYG",
                "type": "filterpane",
                "col": 0,
                "row": 8,
                "colspan": 3,
                "rowspan": 4
              },
              {
                "name": "VtfsZDc",
                "type": "barchart",
                "col": 3,
                "row": 4,
                "colspan": 10,
                "rowspan": 4
              },
              {
                "name": "TqwwFf",
                "type": "scatterplot",
                "col": 3,
                "row": 8,
                "colspan": 10,
                "rowspan": 4
              },
              {
                "name": "LXAaTP",
                "type": "pivot-table",
                "col": 13,
                "row": 4,
                "colspan": 11,
                "rowspan": 4
              },
              {
                "name": "EpsDdJ",
                "type": "table",
                "col": 13,
                "row": 8,
                "colspan": 11,
                "rowspan": 4
              }
            ],
            "title": "Budget Analysis",
            "labelExpression": "",
            "showCondition": "",
            "description": "Analyze actual versus budget budget data. Is the company on target to hit its budgeted amounts?",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "0c9d71bd-02a5-4939-8d79-3b0ff8337588",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "My new sheet",
            "description": ""
          },
          "qData": {
            "rank": 5,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "NJPEk",
                "type": "qlik-date-picker",
                "col": 0,
                "row": 0,
                "colspan": 12,
                "rowspan": 6,
                "bounds": {
                  "y": 0,
                  "x": 0
                  "width": 50,
                  "height": 50
                }
              },
              {
                "name": "amYnj",
                "type": "qlik-on-demand-reporting",
                "col": 0,
                "row": 6,
                "colspan": 12,
                "rowspan": 6,
                "bounds": {
                  "y": 50,
                  "x": 0,
                  "width": 50,
                  "height": 50
                }
              },
              {
                "name": "qNVhQV",
                "type": "SO_65505874",
                "col": 12,
                "row": 0,
                "colspan": 12,
                "rowspan": 6,
                "bounds": {
                  "y": 0,
                  "x": 50,
                  "width": 50,
                  "height": 50
                }
              }
            ],
            "title": "My new sheet",
            "labelExpression": "",
            "showCondition": "",
            "description": "",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "38d68a2c-a6e5-437e-b2f5-9df4bfeb39fa",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "My new sheet (1)",
            "description": ""
          },
          "qData": {
            "rank": 6,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "vhZQaT",
                "type": "linechart",
                "col": 0,
                "row": 0,
                "colspan": 15,
                "rowspan": 6,
                "bounds": {
                  "y": 0,
                  "x": 0,
                  "width": 62.5,
                  "height": 50
                }
              },
              {
                "name": "mKHFyU",
                "type": "filterpane",
                "col": 15,
                "row": 0,
                "colspan": 9,
                "rowspan": 6,
                "bounds": {
                  "y": 0,
                  "x": 62.5,
                  "width": 37.5,
                  "height": 50
                }
              },
              {
                "name": "ppRgu",
                "type": "filterpane",
                "col": 0,
                "row": 6,
                "colspan": 12,
                "rowspan": 6,
                "bounds": {
                  "y": 50,
                  "x": 0,
                  "width": 50,
                  "height": 50
                }
              },
              {
                "name": "Upa",
                "type": "filterpane",
                "col": 12,
                "row": 6,
                "colspan": 12,
                "rowspan": 6,
                "bounds": {
                  "y": 50,
                  "x": 50,
                  "width": 50,
                  "height": 50
                }
              }
            ],
            "title": "My new sheet (1)",
            "labelExpression": "",
            "showCondition": "",
            "description": "",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        },
        {
          "qInfo": {
            "qId": "8181d8b2-877a-4e8e-a26d-96f79124a95e",
            "qType": "sheet"
          },
          "qMeta": {
            "privileges": [
              "read",
              "update",
              "delete",
              "exportdata",
              "change_owner"
            ],
            "title": "My new sheet (2)",
            "description": ""
          },
          "qData": {
            "rank": 7,
            "columns": 24,
            "rows": 12,
            "cells": [
              {
                "name": "xTbFH",
                "type": "text-image",
                "col": 0,
                "row": 0,
                "colspan": 12,
                "rowspan": 2,
                "bounds": {
                  "y": 0,
                  "x": 0,
                  "width": 50,
                  "height": 16.666666666666664
                }
              },
              {
                "name": "mMdGJAS",
                "type": "filterpane",
                "col": 0,
                "row": 2,
                "colspan": 13,
                "rowspan": 7,
                "bounds": {
                  "y": 16.666666666666664,
                  "x": 0,
                  "width": 54.166666666666664,
                  "height": 58.333333333333336
                }
              },
              {
                "name": "fypwrW",
                "type": "table",
                "col": 13,
                "row": 0,
                "colspan": 11,
                "rowspan": 6,
                "bounds": {
                  "y": 0,
                  "x": 54.166666666666664,
                  "width": 45.83333333333333,
                  "height": 50
                }
              }
            ],
            "title": "My new sheet (2)",
            "labelExpression": "",
            "showCondition": "",
            "description": "",
            "descriptionExpression": "",
            "thumbnail": ""
          }
        }
      ]
    }
  }
}
```