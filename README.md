name: Run-Bot-VPS
on: [workflow_dispatch]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Start VPS Server
        run: |
          echo "جاري تشغيل السيرفر يا أبو بطة..."
          python3 --version
          pip install freqtrade
          freqtrade --version
          echo "السيرفر جاهز والحمد لله!"
