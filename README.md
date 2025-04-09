# notify-action

Notify Action for GitHub Actions

### Usage

- **Settings** > **Actions secrets and variables**
    - `NOTIFY_URL`
    - `NOTIFY_KEY`
- Add step to GitHub Actions workflow
  ```yaml
  - name: Send Notification
    uses: matidev/notify-action@v1
    if: ${{ success() }}
    with:
      notifyUrl: ${{ secrets.NOTIFY_URL }}
      notifyKey: ${{ secrets.NOTIFY_KEY }}
  ```