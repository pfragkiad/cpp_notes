
### Common operations

## Sum product of two vectors

```c++
#include <numeric>
#include <vector>
#include <iostream>


int main(int argc, char** argv)
{
	//fill range with values from 0 to 2
	std::vector<int> range(3); std::iota(range.begin(), range.end(), 0);
	//initialize vectors v1, v2
	std::vector<double> v1{ 1.0,2.0,3.0 }, v2{ 1.0,2.0,3.0 };
	std::cout << std::accumulate(range.cbegin(), range.cend(), 0.0,
		[&](double sum, int i) {return sum + v1[i] * v2[i]; });
}
```
