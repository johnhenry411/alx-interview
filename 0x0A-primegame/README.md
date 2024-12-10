# 🎮 Prime Game: Maria vs. Ben 🧮

Welcome to the **Prime Game** repository, where Maria and Ben battle it out in a game of strategy, primes, and... questionable coding decisions. 🥳 This is your one-stop shop for all things prime, quirky, and mildly confusing. Buckle up, it's going to be a bumpy ride! 🚀

---

## 📜 What's this game about?  

Maria and Ben play a game based on **prime numbers**. Here's the gist:

- They play `x` rounds. 🎲  
- In each round, they take turns choosing numbers from a list (`nums`) and removing their multiples until no numbers are left.  
- The one who removes the most numbers wins that round. 👑  
- Maria starts first because... she's Maria. 🧠✨  

---

## ⚙️ How to Play

Simply call the function `isWinner(x, nums)` with:  
- `x`: Number of rounds to play. 🕹️  
- `nums`: A list of numbers representing the game state for each round. 🧮  

The function will return the ultimate winner:  
- `"Maria"` if she's the prime queen 👸.  
- `"Ben"` if he outsmarts her 🤴.  
- `None` if it's a tie or your input is bad, you cheater. 😤  

---

## 🛠️ Code Breakdown (aka *The Fun Part*)  

### 🧩 Main Function: `isWinner`
- **Purpose**: Decides who wins after `x` rounds. 🏆  
- **Logic**:  
  1. **Input sanity check**: If the inputs are bogus, we bow out early. 🛑  
  2. **Prime Time Setup**: We create a sieve to identify primes (because who doesn’t love a good sieve?). 🍝  
  3. **Scorekeeping**: Maria and Ben battle it out over primes. 📈  
  4. **Winner Declaration**: A glorious proclamation of victory. 📣  

### 🍝 Helper Function: `rm_multiples`  
- **Purpose**: Eliminates multiples of a given number from the list, leaving only the juicy primes.  
- **Caveat**: May or may not cause existential crises for numbers that aren't primes. 🤔  

---

## 🤡 Fun Stuff  

- **Edge Cases**: This function isn’t just for playing—it’s a life lesson in handling nonsense inputs gracefully. 🌟  
  ```python
  isWinner(0, None)  # Returns None because nobody has time for that.
  ```
- **Prime Whispering**: Did you know? The sieve starts with `[1, 1, 0, 0...]` because apparently, 0 and 1 don’t get to join the prime party. 🙅‍♂️  

---

## ⚠️ Disclaimer

- **No guarantees on fairness**: The code seems pretty biased toward primes. If you’re not a fan of primes, this might not be the game for you. 😅  
- **Humor not included**: Wait, yes it is.  

---

## 📣 Call to Action

Feeling lucky? 🍀 Want to prove you're smarter than a Python script? Test it out now!  

Happy coding and may the best prime enthusiast win! 🥳