# Tabulation
Rod-Cutting Problem
![Screenshot 2025-04-03 212739](https://github.com/user-attachments/assets/7bee349f-ebed-4fb2-8858-bdd9c88c9699)
> [!NOTE]
> Prices of each size of cut rod are stored in list “prices” of length = n+1 with price corresponding to spot in list and 0-spot initialized at 0. (Ex: Price for $3 rod will be stored at price[3].)

> [!NOTE]
>Tabulation list “max_prices” is initialized as a list of length = 1 with max_prices[0] = 0 to correspond with the price of “zero-inch” rod. New values are appended onto the tabulation list until max_prices[n], creating a list of length = n+1.

> [!IMPORTANT]
> Function find_max_price iterates through 2 loops. The outer loop (using iterator “i”) is used to iterate up one spot in max_prices to determine the value needed in max_prices[i]. The inner loop (using iterator “j”) is used to find the maximum value of all possible combination of cuts in each max_prices[i] and then append that value to max_prices at max_prices[i]. This is done by finding the maximum between any combination of previously reached values with the single rod price needed to reach the current “i” value.

> [!WARNING]
>Time Complexity:
Two loops are iterated over the length of n, (n*n)
>Space Complexity:
Two lists of n+1 are used to store values, (2(n+1)
