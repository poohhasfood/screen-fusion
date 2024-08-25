//palindrome code for c++

#include <iostream>

bool isPalindrome(int x) {
    // Handle negative numbers
    if (x < 0) return false;

    int reversed = 0;
    int temp = x;  // Use a temporary variable to store the value of x

    // Reverse the number
    while (temp != 0) {
        int digit = temp % 10;  // Get the last digit
        reversed = reversed * 10 + digit;  // Add digit to the reversed number
        temp /= 10;  // Remove the last digit from temp
    }

    // Check if the reversed number is equal to the original
    return x == reversed;
}

int main() {
    int x = 121;  // Example input
    if (isPalindrome(x)) {
        std::cout << x << " is a palindrome." << std::endl;
    } else {
        std::cout << x << " is not a palindrome." << std::endl;
    }

    return 0;
}
