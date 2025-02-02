# Trotter-Suzuki Error Scaling

The **Trotter-Suzuki decomposition** improves the accuracy of quantum simulations by increasing the order of the formula. The higher the order, the smaller the error, but at the cost of more exponentials.

## Error Scaling Table

| Order \( 2k \) | Error Scaling \( O(\Delta t^n) \) | Number of Exponentials \( N \) |
|--------------|----------------------|-------------------|
| 1st (Trotter) | \( O(\Delta t^2) \)  | \( O(1) \) |
| 2nd (Suzuki) | \( O(\Delta t^4) \)  | \( 3 \) |
| 4th  | \( O(\Delta t^6) \)  | \( 7 \) |
| 6th  | \( O(\Delta t^8) \)  | \( 19 \) |
| 8th  | \( O(\Delta t^{10}) \) | \( 49 \) |
| 10th  | \( O(\Delta t^{12}) \) | \( 123 \) |
| \( 2k \)th  | \( O(\Delta t^{2k+2}) \) | \( O(5^k) \) |

## Observations:
- Increasing the order **significantly reduces error**.
- However, the **number of exponentials grows exponentially**, following \( O(5^k) \), making high-order formulas computationally expensive.

