## Description

How to retrieve all bookmarks (for the currently authenticated user) for an app

## Code

```JavaScript
const objProperties = {
  qInfo: { qId: "BookmarkList", qType: "BookmarkList" },
  qBookmarkListDef: {
    qType: "bookmark",
    qData: {
      title: "/qMetaDef/title",
      description: "/qMetaDef/description",
      sheetId: "/sheetId",
      selectionFields: "/selectionFields",
      creationDate: "/creationDate",
    },
  },
};

const obj = await app.createSessionObject(objProperties);

const objLayout = await obj.getLayout();
```

## Response structure (overall)

![[Pasted image 20230725075230.png]]

## Response structure (single bookmark)

![[Pasted image 20230725075404.png]]

## Example response (full)

```json
{
    "qInfo": {
        "qId": "482fb457-5361-4abf-8f8f-8e61f3dd1a90",
        "qType": "BookmarkList"
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
    "qBookmarkList": {
        "qItems": [
            {
                "qInfo": {
                    "qId": "1c12bf8f-f4f8-4c77-be25-50838ca4c8f7",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "Bookmark11",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "=state_name=ValueList('Minnesota')",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44261.27836805556,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "Bookmark11",
                    "description": "",
                    "sheetId": "JzJMza",
                    "selectionFields": "state_name",
                    "creationDate": "2021-03-06T06:40:51.914Z"
                }
            },
            {
                "qInfo": {
                    "qId": "b126dc6e-4eb8-4454-b2df-3fbe0378eb28",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "Bookmark12",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44261.4315625,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "Bookmark12",
                    "description": "",
                    "sheetId": "JzJMza",
                    "selectionFields": "state_name",
                    "creationDate": "2021-03-06T10:21:27.275Z"
                }
            },
            {
                "qInfo": {
                    "qId": "4eb20470-1eab-427b-bf7f-1f2a89d8d0c3",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "Bookmark13",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44261.43204861111,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "Bookmark13",
                    "description": "",
                    "sheetId": "JzJMza",
                    "selectionFields": "state_name",
                    "creationDate": "2021-03-06T10:22:09.288Z"
                }
            },
            {
                "qInfo": {
                    "qId": "17a2dd66-1c7a-4c9b-a970-68c8f8090dd3",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "Bookmark Multiple",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "Product Group Desc",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Sales Rep Name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "=state_name=ValueList('Minnesota')",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44261.80396990741,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "Bookmark Multiple",
                    "description": "",
                    "sheetId": "JzJMza",
                    "selectionFields": "Product Group Desc, Sales Rep Name, state_name",
                    "creationDate": "2021-03-06T19:17:43.891Z"
                }
            },
            {
                "qInfo": {
                    "qId": "8a1480e4-5cb2-47d5-848b-ec8473cc0a05",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "Bookmark Multiple 1",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "Product Group Desc",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Regional Sales Mgr Name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "*a*",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Sales Rep Name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "=state_name=ValueList('Minnesota')",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44261.907013888886,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "Bookmark Multiple 1",
                    "description": "",
                    "sheetId": null,
                    "selectionFields": "Product Group Desc, Regional Sales Mgr Name, Sales Rep Name, state_name",
                    "creationDate": "2021-03-06T21:46:06.023Z"
                }
            },
            {
                "qInfo": {
                    "qId": "7a660b12-fb35-47e0-a50a-2af22c8199a4",
                    "qType": "bookmark"
                },
                "qMeta": {
                    "title": "6+ fields",
                    "description": "",
                    "privileges": [
                        "read",
                        "update",
                        "delete",
                        "exportdata"
                    ]
                },
                "qData": {
                    "qBookmark": {
                        "qStateData": [
                            {
                                "qStateName": "$",
                                "qFieldItems": [
                                    {
                                        "qDef": {
                                            "qName": "Month",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Customer",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Product Group Desc",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Product Sub Group Desc",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Regional Sales Mgr Name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "*a*",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Sales Rep Name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "state_name",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qTextSearch": "=state_name=ValueList('Minnesota')",
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    },
                                    {
                                        "qDef": {
                                            "qName": "Line Desc 1",
                                            "qType": "PRESENT"
                                        },
                                        "qSelectInfo": {
                                            "qRangeLo": "NaN",
                                            "qRangeHi": "NaN",
                                            "qNumberFormat": {
                                                "qType": "U",
                                                "qnDec": 10,
                                                "qUseThou": 0
                                            },
                                            "qRangeInfo": [],
                                            "qContinuousRangeInfo": []
                                        },
                                        "qValues": [],
                                        "qExcludedValues": []
                                    }
                                ]
                            }
                        ],
                        "qUtcModifyTime": 44263.19043981482,
                        "qVariableItems": [],
                        "qPatches": []
                    },
                    "title": "6+ fields",
                    "description": "",
                    "sheetId": "jDSPJ",
                    "selectionFields": "Month, Customer, Product Group Desc, Product Sub Group Desc, Regional Sales Mgr Name, Sales Rep Name, state_name, Line Desc 1",
                    "creationDate": "2021-03-08T04:34:14.796Z"
                }
            }
        ]
    }
}
```