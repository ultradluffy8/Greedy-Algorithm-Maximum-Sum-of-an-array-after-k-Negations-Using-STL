# Greedy-Algorithm-Maximum-Sum-of-an-array-after-k-Negations-Using-STL

/*Maximum Sum of an array after k Negations
              Using STL            
.
.
.
.
.
.
.
.
.
.
.
.
.
.
*/
#include<bits/stdc++.h>
using namespace std;
typedef long long ll;

int main() {
	ll k, n;
	cin >> n >> k;
	vector<int> v;
	while (n--) {
		ll t;
		cin >> t;
		v.push_back(t);
	}
	while (k--) {
		*min_element(v.begin(), v.end()) = -*min_element(v.begin(), v.end());
	}
	ll sum = 0;
	for (auto x : v) {
		sum += x;
	}
	cout << sum;

	return 0;
}
