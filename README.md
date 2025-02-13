# Sublime-Text

# ST Competitive Programming Setup In C++

⚫  Copy the Path In Environment variables → C:\Program Files\MinGW\bin

⚫  Open Command Prompt And Check :

            1. path

            2. g++

⚫  Open Sublime Text : 

1. Create 3 New Files ( demo.cpp , input.txt, outpu.txt )
2. Go To View → Layout → Columns: 3
3. Go To View → Groups → Max Columns: 2

# Tools → Build System  → New Build System

## 1. CP.build-system

```
{
    "cmd": ["g++.exe", "-std=c++17", "${file}",
    "-o", "${file_base_name}.exe",
    "&&", "${file_base_name}.exe<inputf.in>outputf.out"],
    "shell":true,
    "working_dir":"$file_path",
    "selector":"source.cpp"
}
```

## 2. Testing Code :
  → Copy And Paste 👇🏻
       
```cpp
#include <iostream>
using namespace std;

void init_code() {
ios_base::sync_with_stdio(false);
cin.tie(NULL);
#ifndef ONLINE_JUDGE
freopen("input.txt", "r", stdin);
freopen("output.txt", "w", stdout);
#endif
}

int main() {
init_code();


int a, b;
cout << "Enter two numbers: ";
cin >> a >> b;
cout << "Sum: " << a + b << endl;

return 0;

}
```
⚫ Give Inputs: Any 2 Numbers !

## 3. Run Command → ctrl + c
