# zim-build

This branch holds only `.github/workflows/docs-zim.yml`, which builds the Meshtastic
documentation (meshtastic/meshtastic) into a Kiwix ZIM with
[docusaurus2zim](https://github.com/NomDeTom/docusaurus2zim) and its `examples/meshtastic.json`.
It shares no history with `master`, so pushing here runs none of upstream's workflows.

- **Test:** push to this branch. It builds `meshtastic/meshtastic@master` and uploads the ZIM as
  a run artifact.
- **Build another ref or publish:** Actions → "Meshtastic docs ZIM" → Run workflow, with a
  `docs_ref` and `publish` ticked. That attaches `meshtastic-docs.zim` to a release tagged
  `meshtastic-docs-<date>-<commit>`, which an Irate-Box hub installs with
  `sudo ./install.sh --zim <asset URL>`.
