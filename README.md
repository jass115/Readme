### 3. What this proof is claiming is correct, but there's something in the proof that's wrong. Find that incorrect statement in the proof:
We want to disprove that N7 = O(N4). For this to be tree, it must be the case that N7 ≤ c * N4 for some c > 0. But N7 ≤ N4 won't be true ever because the 7 exponent causes N7 to always be bigger.

This prove would be correct if N7 is greater than or equal to N4 otherwise if we use the same condition its just hard to figure how we can fix that.

#### 4. Write the recurrence relation for the reverse(L) function:
append(x, L) 
{ Node curr = L;   // T(n)
while(curr != null && curr.next != null) {
curr = curr.next; } 
curr.next = x; 
}
reverse(L){
if(L == null)      // null means nothing so 0 L = 0 return null;
}
else {
Node front = L;     //1 
Node rest = L.next;
L.next = null; 
Node restReversed = reverse(rest); // reverse relationship so it would be T(n-1)
append(font, restReversed);
}
 I think the recurrence relation is T(n) = 0 because of the null and T(n) = T(n-1)+1

##### 5. What is the runtime of the following code snippet, in tight Big-O notation?
    int count = 0;
    for (int i = N; i > 0; i /= 2) {
        for (int j = 0; j < i; j++) {
            count += 1;
        }
    }
The big o notation is O(NlogN) I think its that becuase for first loop its O(logN) and for second loop its O(N) and if we joined it together e got O(NlogN
