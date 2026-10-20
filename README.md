# Onedrive

The owner's OneDrive, organized into projects and notebooks. Nothing of the drive is kept on main: the catalog, the proposals, the moves and the notebooks live on the branch drive-catalog, and this repository stays private because they name the owner's files.

## Reading the drive

The drive is read through Microsoft Graph under the owner's own Microsoft sign-in, never through a page's or an extension's session.

1. Sign in once: open https://openspineconsortium.com/symphony/control/, choose OpenSpineConsortium/onedrive in the bar, open the Folders tab, press Connect OneDrive and sign in with the Wayne State account, then press Track. That seals the sign-in into this repository's secret SYMPHONY_DRIVE_REFRESH.
2. On the owner's word, run Actions, Drive catalog, Run workflow. It writes catalog.json, TREE.md and digests.jsonl as one commit on top of drive-catalog and keeps everything else there.

The workflow's tools (tools/drive_organize.py, tools/drive_sync.py, tools/file_digest.py and tools/sdlc_protocol) are copies of OpenSpineConsortium/symphony-template's at commit b8954fd2f4e4, where they are changed and tested; bring a newer copy here by pull request. Nothing on the drive moves or is renamed without the owner's go.
