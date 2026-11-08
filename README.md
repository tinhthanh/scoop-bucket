# Vetgo Scoop bucket

[Scoop](https://scoop.sh) manifests for [Vetgo](https://github.com/tinhthanh/shipyard), a fork of Shipyard: run coding agents on your own boxes.

Scoop needs git to add a bucket (`scoop install git`, once):

```powershell
scoop bucket add vetgo https://github.com/tinhthanh/scoop-bucket
scoop install vetgo/vetgo
berth agent install      # the laptop agent, started when you sign in
```

`vetgo` installs `berth`, the CLI and laptop agent, with the daemons it puts on boxes. Each fork release updates `bucket/vetgo.json` (written by `scripts/scoop-manifest.py` in tinhthanh/shipyard's release workflow). After an update, `berth agent restart --if-stale` moves a running agent to the new version.

The desktop app is installed separately: `irm https://tinhthanh.github.io/shipyard/install.ps1 | iex`.
