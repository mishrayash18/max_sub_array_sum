# max_sub_array_sum
this contains all three approaches of max sub array sum problem and the most optimised approach has the use of kadane's algorithm

// // SUB ARRAYS BRUTE FORCE METHOD
// #include <iostream>
// #include <vector>
// using namespace std;

// int main() {
//     int size = 5;
//     int array[5] = {1,2,3,4,5};

//     for (int st=0; st<size; st++) {
//         for (int end=st; end<size; end++) {
//             for (int i=st; i<=end; i++) {
//                 cout << array[i];
//             }
//             cout << " ";
//         }
//         cout << endl;
//     }
// }









// MAX SUB ARRAY SUM SLIGHTLY OPTIMISED BRUTE FORCE
// #include <iostream>
// #include <vector>
// using namespace std;

// int main() {
//     int maxsum = INT16_MIN;
//     int size = 7;
//     int array[7] = {3, -4, 5, 4, -1, 7, -8};
//     for (int st=0; st<size; st++) {
//         int currsum = 0;
//         for (int end=st; end<size; end++) {
//             currsum += array[end];
//             maxsum = max(currsum, maxsum);
//         }
//     }
//     cout << maxsum;
//     return 0;
// }










// // MAX SUB ARRAY SUM USING KADANE'S ALGO (MOST OPTIMISED)
// #include <iostream>
// using namespace std;
// int main() {
//     int size = 7;
//     int array[7] = {3, -4, 5, 4, -1, 7, -8};
//     int maxsum = INT16_MIN;
//     int currsum = 0;

//     for (int i=0; i<size; i++) {
//         currsum += array[i];
//         maxsum = max(currsum, maxsum);
//         if (currsum<0) {
//             currsum=0;
//         }
//     }
//     cout << maxsum;
//     return 0;
// } 
