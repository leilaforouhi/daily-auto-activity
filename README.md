import datetim
import json
import os

def save_log():
    today = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    data = {"last_run": today}

    with open("activity_log.json", "w") as f:
        json.dump(data, f, indent=4)

    print("Activity logged at:", today)

if __name__ == "__main__":
    save_log()
