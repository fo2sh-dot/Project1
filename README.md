import threading
import time

def numbers():
    for i in range(1, 6):
        print("Number:", i)
        time.sleep(0.3)

def letters():
    for c in ["A", "B", "C", "D", "E"]:
        print("Letter:", c)
        time.sleep(0.3)

t1 = threading.Thread(target=numbers)
t2 = threading.Thread(target=letters)

t1.start()
t2.start()

t1.join()
t2.join()

print("Threading Finished")
