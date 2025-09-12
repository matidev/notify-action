# notify-action

Notify Action for GitHub Actions

_It is only used for [MatiPlus](https://mati.plus/?utm_source=github-notify-action) or partner projects._

### Usage

- **Settings** > **Actions secrets and variables**
    - `NOTIFY_URL`
    - `NOTIFY_KEY`
- Add step to **GitHub Actions** workflow
  ```yaml
  - name: Send Notification
    uses: matidev/notify-action@latest
    if: ${{ success() }}
    with:
      notifyUrl: ${{ secrets.NOTIFY_URL }}
      notifyKey: ${{ secrets.NOTIFY_KEY }}
  ```
- Can use `targetBranch` is optional.