# showCollections()

List all collections or get collection loading status.

## Invocation

```javascript
new milvusClient(MILUVS_ADDRESS).collectionManager.showCollections(
  ShowCollectionsReq
);
```

## Parameter

### ShowCollectionsReq

| Parameter       | Description                                                                            | type                |
| --------------- | -------------------------------------------------------------------------------------- | ------------------- |
| collection_name | Name of the collections to check for their loading status                              | String[]        |
| type            | ShowCollectionsType                                                                    | ShowCollectionsType |
| timeout?        | An optional duration of time in millisecond to allow for the RPC. Default is undefined | Number              |

### ShowCollectionsType

| value | Description | type   |
| ----- | ----------- | ------ |
| 0     | All         | number |
| 1     | Loaded      | number |

## Example

```javascript
import { MilvusClient } from "@zilliz/milvus2-sdk-node";

new milvusClient(MILUVS_ADDRESS).collectionManager.showCollections();
```

## Return

```javascript
// showCollections return
{
  status: { error_code: 'Success', reason: '' },
  data: [
    {
      name: 'my_collection',
      id: '434826867399720961',
      timestamp: '1658732862090',
      loadedPercentage: undefined
    }
  ]，
  created_timestamps: [ '434826867399720964' ],
  created_utc_timestamps: [ '1658732862090' ],
}
```
