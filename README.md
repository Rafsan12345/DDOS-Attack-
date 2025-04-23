# file: load_test.py
import requests
import threading

def send_request():
    try:
        res = requests.get("http:......")
        print(f"Status: {res.status_code}")
    except Exception as e:
        print(f"Error: {e}")

# 50 টি থ্রেড চালিয়ে একসাথে রিকোয়েস্ট পাঠানো
while(1):

  for i in range(1000):
      t = threading.Thread(target=send_request)
      t.start()
