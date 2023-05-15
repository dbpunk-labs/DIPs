# DB3 Network:A Decentralized and Scalable Data-Rollup Data Network



db3 network is a fully decentralized data network. You can fully control your data, nobody can delete or modify your data and you can reach your data from any application in the db3 network. db3 network has the following technology features
```mermaid
graph TD
    subgraph protocol
        A[Social Protocol] --> SDK(DB3.js)
        B[Game Protocol] -->SDK(DB3.js)
        C[Dao Tools] --> SDK(DB3.js)
        style protocol fill:#fff,stroke:#333,stroke-width:1px
    end

    subgraph layer2
        subgraph blocks
            subgraph Block1
                direction LR
                E1 --> E3
                E2 --> E3
                style Block1 fill:#fff,stroke:#333,stroke-width:1px
            end
            subgraph Block2
                direction LR
                D1 --> D3
                D2 --> D3
                style Block2 fill:#fff,stroke:#333,stroke-width:1px
            end
            subgraph Block3
                direction LR
                F1 --> F3
                F2 --> F3
                F3 --> F4
                style Block3 fill:#fff,stroke:#333,stroke-width:1px
            end
            Block2 --> Block1
            Block3 --> Block2
            direction RL
            style blocks fill:#fff,stroke:#333,stroke-width:1px
        end
        subgraph indexer
            Btree
            Graph
            Vector
            style indexer fill:#fff,stroke:#333,stroke-width:1px
        end
        blocks --> indexer
        style layer2 fill:#fff,stroke:#333,stroke-width:1px
        direction LR
    end

    subgraph layer1
        L1
        Arweave
        style layer1 fill:#fff,stroke:#333,stroke-width:1px
    end

    protocol --> layer2
    layer2 --> |Rollup|layer1
```

* `Permanent Level  Data Availability`, data availability is the most important things in the decentralized network and db3 network uses arweave as a long term data availability layer to achieve the permanent level data availability
* `AR-Rollup`, db3 network itself will act a short term data availability layer and uses ar-rollup to improve the write throughput, reduce the storage cost and support privacy protection
* `Web2 Developer Experience`, you can use db3.js like using firebase sdk

## DIPS
| title   |    author     | status |
|----------|-------------|---------|
|[DIP-000: Structured Binary Data Format](./dips/dip-000.md)| [imotai](https://github.com/imotai) | wip |

## Contribution

if you are interested in db3 network, you can propose an improvement propsal here
