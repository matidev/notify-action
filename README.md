# notify-action

A lightweight GitHub Action for sending structured notifications to an external endpoint.

> _This action is intended for use with [MatiPlus](https://matiplus.com/?utm_source=github-notify-action) and partner
projects._

### Usage

1. Configure Repository Secrets

   Go to **Settings → Secrets and variables → Actions → Repository secrets** and add:
    - `NOTIFY_URL`
    - `NOTIFY_KEY`

2. Add the following step to your **GitHub Actions** workflow file

    ```yaml
    - name: Send Notification
      uses: matidev/notify-action@latest
      if: ${{ success() }}
      with:
        notifyUrl: ${{ secrets.NOTIFY_URL }}
        notifyKey: ${{ secrets.NOTIFY_KEY }}
    ```
   > _Can use `targetBranch` is optional.
   > If provided, it will override the `ref_name` value in the payload_

### Publishing to `latest` Tag

```bash
git tag -f latest
git push origin latest --force
```