# CTDL-GT_Selection_Sort_1.cpp
Selection Sort
Nguồn tham khảo : https://freetuts.net/thuat-toan-sap-xep-chon-selection-sort-2931.html
Cài đặt Selection Sort:

void selectionSort(int arr[], int n)
{
    int i, j, min_idx;
    // Di chuyển ranh giới của mảng đã sắp xếp và chưa sắp xếp
    for (i = 0; i < n-1; i++)
    {
    // Tìm phần tử nhỏ nhất trong mảng chưa sắp xếp
    min_idx = i;
    for (j = i+1; j < n; j++)
        if (arr[j] < arr[min_idx])
        min_idx = j;
  
    // Đổi chỗ phần tử nhỏ nhất với phần tử đầu tiên
        swap(arr[min_idx], arr[i]);
    }
}
Hàm swap : //đổi chỗ 

void swap(int &xp, int &yp)
{
    int temp = xp;
    xp = yp;
    yp = temp;
}
