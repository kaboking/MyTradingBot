name: Abu-Batta-Bot
on: [workflow_dispatch]
jobs:
  trade:
    runs-on: ubuntu-latest
    steps:
      - name: Start Server
        run: |
          echo "يا محمد السيرفر بدأ يشتغل حالاً.."
          python3 -m pip install --upgrade pip
          pip install freqtrade
          echo "مبروك يا أبو بطة.. السيرفر جاهز للصيد!"
