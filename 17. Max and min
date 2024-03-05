def find_max_min(arr, low, high):
    if low == high:
        return arr[low], arr[low]

    mid = (low + high) // 2
    max_left, min_left = find_max_min(arr, low, mid)
    max_right, min_right = find_max_min(arr, mid + 1, high)
    max_val = max(max_left, max_right)
    min_val = min(min_left, min_right)

    return max_val, min_val

my_list = [3, 1, 7, 9, 5, 2, 8, 4, 6]

max_value, min_value = find_max_min(my_list, 0, len(my_list) - 1)

print("Original List:", my_list)
print("Maximum Value:", max_value)
print("Minimum Value:", min_value)
