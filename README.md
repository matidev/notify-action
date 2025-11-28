# notify-action

A lightweight GitHub Action for sending structured notifications to an external endpoint.

>_This action is intended for use with [MatiPlus](https://mati.plus/?utm_source=github-notify-action) and partner
projects._

### Usage

1. Configure Repository Secrets

   Go to **Settings → Secrets and variables → Actions → Repository secrets** and add:
    - `NOTIFY_URL`
    - `NOTIFY_KEY`

2. Add Step to **GitHub Actions** Workflow

    ```yaml
    - name: Send Notification
      uses: matidev/notify-action@latest
      if: ${{ success() }}
      with:
        notifyUrl: ${{ secrets.NOTIFY_URL }}
        notifyKey: ${{ secrets.NOTIFY_KEY }}
    ```
   >_Can use `targetBranch` is optional._