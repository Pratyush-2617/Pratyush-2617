
public class assign {
    public static int removeDuplicates(int[] nums) {
        if (nums == null || nums.length == 0) {
            return 0;
        }

        int k = 1; // Initialize the unique elements count

        for (int i = 1; i < nums.length; i++) {
            if (nums[i] != nums[i - 1]) {
                nums[k] = nums[i];
                k++;
            }
        }

        // Set the remaining elements to unset/undefined/null
        for (int i = k; i < nums.length; i++) {
            nums[i] = 0; // You can set it to any value or leave it as 0/null
        }

        return k;
    }

    public static void main(String[] args) {
        int[] nums1 = {1, 1, 2};
        int resultLength1 = removeDuplicates(nums1);

        System.out.print("Unique elements: ");
        for (int i = 0; i < resultLength1; i++) {
            System.out.print(nums1[i] + " ");
        }

        System.out.println("\nResult length: " + resultLength1);

        int[] nums2 = {0, 0, 1, 1, 1, 2, 2, 3, 3, 4};
        int resultLength2 = removeDuplicates(nums2);

        System.out.print("\nUnique elements: ");
        for (int i = 0; i < resultLength2; i++) {
            System.out.print(nums2[i] + " ");
        }

        System.out.println("\nResult length: " + resultLength2);
    }
}
