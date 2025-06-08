import hashlib

def word_count(text):
    words = text.lower().split()
    count = {}
    for word in words:
        count[word] = count.get(word, 0) + 1
    return count

text = "яблуко груша яблуко банан яблуко груша груша груша банан"
counts = word_count(text)
print("Слова > 3 рази:", [w for w, c in counts.items() if c > 3])

inventory = {"яблуко": 10, "груша": 3, "банан": 2}

def update_inventory(product, amount):
    inventory[product] = inventory.get(product, 0) + amount
    if inventory[product] < 0:
        inventory[product] = 0

update_inventory("груша", 2)
update_inventory("банан", -1)
print("Мало товарів:", [p for p, q in inventory.items() if q < 5])

sales = [
    {"продукт": "яблуко", "кількість": 30, "ціна": 20},
    {"продукт": "груша", "кількість": 10, "ціна": 50},
    {"продукт": "яблуко", "кількість": 25, "ціна": 20},
]

def total_income(sales_list):
    income = {}
    for sale in sales_list:
        name = sale["продукт"]
        income[name] = income.get(name, 0) + sale["кількість"] * sale["ціна"]
    return income

income = total_income(sales)
print("Доходи > 1000:", [p for p, i in income.items() if i > 1000])

tasks = {
    "Завдання 1": "очікує",
    "Завдання 2": "в процесі",
    "Завдання 3": "виконано"
}

def add_task(name, status):
    tasks[name] = status

def remove_task(name):
    tasks.pop(name, None)

def change_status(name, new_status):
    if name in tasks:
        tasks[name] = new_status

print("Очікують:", [t for t, s in tasks.items() if s == "очікує"])

users = {
    "admin": {
        "password": hashlib.md5("1234".encode()).hexdigest(),
        "name": "хтось там татам"
    }
}

def check_login(login, password):
    hashed = hashlib.md5(password.encode()).hexdigest()
    if login in users and users[login]["password"] == hashed:
        print("Вхід успішний для", users[login]["name"])
    else:
        print("Невірний логін або пароль")
