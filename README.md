#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

// Function to check if given array is monotonic
bool isMonotonic(vector<int>& A) {
    vector<int> x = A;
    vector<int> y = A;
    sort(x.begin(), x.end());
    sort(y.rbegin(), y.rend());
    if (x == A || y == A) {
        return true;
    }
    return false;
}

// Driver program
int main() {
    vector<int> A = {6, 5, 4, 4};

    // Print required result
    cout << boolalpha << isMonotonic(A) << endl;

    return 0;
}
