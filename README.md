import os
import asyncio
from telegram import Bot

# دالة إرسال الرسالة
async def send_hammo_update():
    # سحب البيانات من الـ Secrets اللي إنت حطيتها في إعدادات GitHub
    token = os.getenv('TG_TOKEN')
    chat_id = os.getenv('TG_CHAT_ID')
    
    if token and chat_id:
        try:
            bot = Bot(token=token)
            # الرسالة اللي هتوصلك على الموبايل
            text_msg = "🚀 يا محمد! حمو بيمسي عليك.. الموتور شغال والربط مع التليجرام 100% تمام. ✅"
            
            await bot.send_message(chat_id=chat_id, text=text_msg)
            print("📱 تم إرسال رسالة التنبيه بنجاح!")
        except Exception as e:
            print(f"❌ حصل خطأ أثناء الإرسال: {e}")
    else:
        print("⚠️ خطأ: تأكد من إضافة TELEGRAM_TOKEN و TELEGRAM_CHAT_ID في الـ Secrets.")

if __name__ == "__main__":
    asyncio.run(send_hammo_update())
