<details>
<summary>Question 1</summary>
<h3>Sort Array of Three Unique Elements</h3>
  <p>
    Given an array A of N integers with at most three unique elements, write an efficient program to sort A in non-decreasing order.
  </p>
  <hr>
<h3>Input</h3>
  First line contains a single integer N
  <br>
  Second line contains N space separated integers of A
<hr>
<h3>Output</h3>
  Print the elements of sorted A separated by a space
  <hr>
<h3>Constraints</h3>
  1 <= N <= 1.5 * 10^5<br/>
  1 <= A[i] <= 10^9
  <hr>
<h3>Sample Input </h3>
  ```
  5
  4 4 8 1 1
  ```
  <hr>
<h3>Sample Output</h3>
  `
  1 1 4 4 8 
  `
</details>

<details>
  <summary>Question1 - Solution</summary>
 <pre>
    #include <bits/stdc++.h>
    using namespace std;

      int main(){
          int n;
          cin>>n;
          int arr[n];
          for(int i=0;i<n;i++) cin>>arr[i];
          // find the frequency of each of the three elements
          map <int,int> m;
          for(int i=0;i<n;i++){
              m[arr[i]]++;
          }
          int count=0;
          for(auto i:m){
              for(int j=0;j<i.second;j++){
                  arr[count++]=i.first;
              }
          }
          for(int i=0;i<n;i++) cout<<arr[i]<<" ";
          return 0;
      }
 </pre>
</details>
