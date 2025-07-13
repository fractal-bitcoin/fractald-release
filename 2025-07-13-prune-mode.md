
# 2025.07 Fractal Prune Mode Explained

## 💡 Recommended Prune Configuration

To optimize disk usage, we recommend keeping ~30GB of recent blocks. You can do this by updating your `bitcoin.conf` as follows:

```
prune=30000     # Retains ~30GB of recent blocks
txindex=0       # Required when pruning (default is 0)
```

With this configuration, the total disk usage of prune mode is expected to be around 300GB, mainly used by:

```
30G   data/blocks
191G  data/chainstate
```

## ⚠️ Important Notes on Pruning Existing Nodes

If you're enabling prune mode from an existing full node, note that:

A legacy `txindex` folder (~153GB) will remain under `data/indexes/txindex`.

- ✅ It is safe to delete this folder in prune mode
- 🧹 Manual cleanup required

This step helps reclaim significant disk space if you’re converting a full node to a pruned one.

## release v0.2.3 of prune mode enhancement

- 💾 Lowered minimum pruning height:
 Reduced from 100,000 to 10,000 — allowing nodes to prune more data and save additional disk space

👉 [View full release notes](https://github.com/fractal-bitcoin/fractald-release/releases/tag/v0.2.3)
