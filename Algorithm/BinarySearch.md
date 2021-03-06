# BinarySearch(이진탐색)
- 정렬된 배열의 경우, 절반씩 줄여나가며 탐색
- 1억개의 목록을 선형 탐색하는 경우 최대 1억번의 연산이 필요하지만, 이진탐색의 경우 27번이면 충분하다
- log2(1억) = 26.xxx

## Binary Search 구현
- 재귀 함수를 이용한 구현
```C
    int binarySearch(vector<int> &nums, int target, int start, int end) {
        if (start > end)
            return -1;
        
        int mid = (start+end) / 2;
        
        if (nums[mid] < target)
            return binarySearch(nums, target, mid+1, end);
        else if (nums[mid] > target) 
            return binarySearch(nums, target, start, mid-1);
        else
            return mid;
    }
```

- 반복문을 이용한 구현
```C
int binarySearch(int arr[], int target) {
    int low = 0;
    int high = arr.length - 1;
    int mid;

    while(low <= high) {
        mid = (low + high) / 2;

        if (arr[mid] == target)
            return mid;
        else if (arr[mid] > target)
            high = mid - 1;
        else
            low = mid + 1;
    }
    return -1;
}
```