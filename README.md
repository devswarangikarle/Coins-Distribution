# Coins-Distribution
Raj has three sisters: Ina, Bina, and Mina. They are collecting coins. Currently, Ina has a coins, Bina has b coins, and Mina has c coins. Recently, Raj has returned from a trip around the world and brought n coins. He wants to distribute all these n coins between his sisters in such a way that the number of coins Ina has is equal 

def can_distribute_coins(a, b, c, n):
    total_sisters_coins = a + b + c
    total_coins = total_sisters_coins + n

    if total_coins % 3 == 0 and n >= max(a, b, c) - a + max(a, b, c) - b + max(a, b, c) - c:
        return "YES"
    else:
        return "NO"

a, b, c, n = map(int, input().split())

result = can_distribute_coins(a, b, c, n)
print(result)
