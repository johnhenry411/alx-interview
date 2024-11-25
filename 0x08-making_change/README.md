# 0x08-making_change
# 🪙 **MakeChange Function** 💰

Welcome to the **MakeChange** repository! 🎉 Here, we tackle the age-old problem: **"How do I break this darn total with the fewest coins?"** 🤔💸

## 🔍 **What's This?**
This Python script contains a single heroic function: **`makeChange`**. 🦸‍♂️ It takes a list of coin denominations (`coins`) and a `total` amount you want to make. Your job? Sit back while `makeChange` figures out how to do it with the fewest number of coins! 🙌

---

## 🛠 **How Does It Work?**
The **`makeChange`** function:
1. 🪙 **Sorts your coins from largest to smallest.** Why start small when you can go big? 😉
2. 🧮 **Greedily subtracts coins from the total** until no more can be subtracted. 
3. 🎯 Returns the fewest number of coins needed to make your total (or some *bad news* 🫠 if it's impossible).

---

## 📜 **Usage**

```python
def makeChange(coins, total):
    """
    Returns: Fewest number of coins needed to meet total
        - If total is 0 or less, return 0 🥳
        - If total cannot be met by any number of coins, return -1 😭
    """
```

### 💡 **Parameters**
- **`coins`**: A list of coin denominations. Example: `[1, 5, 10, 25]` 🪙🪙🪙
- **`total`**: The amount you need to make. Example: `63` 🎯

### 🏁 **Returns**
- **Number of coins**: If you can break the total 💪.
- **`0`**: If the total is 0 or less. Nothing to do here, captain! 🚀
- **`-1`**: If your coins are useless for this total. Sad times. 🥀

---

## 🚨 **Examples**

```python
# Example 1: Can make change
print(makeChange([1, 5, 10, 25], 63)) 
# Output: 6 (25+25+10+1+1+1)

# Example 2: No coins to help
print(makeChange([], 10))
# Output: -1 (Seriously? Give me some coins!)

# Example 3: Total is 0
print(makeChange([1, 2, 5], 0))
# Output: 0 (We’re good here!)

# Example 4: Coins don't fit the bill
print(makeChange([5, 10], 3))
# Output: -1 (Try harder, coins.)
```

---

## 🤔 **Caveats**
- It's greedy. Sometimes, life (and coins) aren't perfect. 🥸
- If you give no coins (`None` or `[]`), it throws in the towel and returns `-1`. What did you expect? 🫠

---

## 🧪 **Testing It**
Clone the repo, run the function, and bask in the glory of optimized change-making. Or cry when you realize you can't make change. Both are valid responses. 🤷‍♂️

---

Happy coin wrangling! 🪙✨