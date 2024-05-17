 int findPair(int n, int x, vector<int> &arr) {
        // code here
          std::sort(arr.begin(), arr.end());
        int i = 0;
        int j = 1;
        while (i < n && j < n) {
            if (i != j && arr[j] - arr[i] == x) {
                return 1;
            }
            if (arr[j] - arr[i] < x) {
                ++j;
            } else {
                ++i;
            }
        }
        return -1;
    }
