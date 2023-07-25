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

const obj = await this.app.createSessionObject(objProperties);

const objLayout = await obj.getLayout();
```