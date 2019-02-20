# pychain   &nbsp; [![Codacy Badge](https://api.codacy.com/project/badge/Grade/43acdb22d1464652bb67540cddad8d21)](https://www.codacy.com/app/AdamHodgson/pychain?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=AdamHodgson/pychain&amp;utm_campaign=Badge_Grade)

Basic implementation of a blockchain in python.

## Usage

### Installation

```
$ python server.py
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```

### Interacting with the Blockchain

GET /chain

```json
{
    "chain": [
        {
            "index": 1,
            "previous_hash": 1,
            "proof": 100,
            "timestamp": 1517160942.196952,
            "transactions": []
        }
    ],
    "length": 1
}
```

GET /mine

```json
{
    "index": 2,
    "message": "New Block Mined",
    "previous_hash": "79a84c98d2e85064113391ce2cd10ca613ff02ee9136c99e28ce7511288d016b",
    "proof": 35293,
    "transactions": [
        {
            "amount": 1,
            "recipient": "c37647f0f5b944698f10a4b81a3e51d3",
            "sender": "0"
        }
    ]
}
```

POST /transactions/new
```json
{
 "sender": "d4ee26eee15148ee92c6cd394edd974e",
 "recipient": "someone-other-address",
 "amount": 5
}
```
```json
{
    "message": "Transaction will be added to block 3"
}
```





## Next steps

1) Add a comprehensive set of unit tests.
2) Transition from PoW to PoS.

## Contributors

Implementation was based on an article by Daniel van Flymen.
