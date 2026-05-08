<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=2ECC71&height=200&section=header&text=Radix%20Sort&fontSize=80&fontColor=ffffff&animation=fadeIn" width="100%" />
</div>

<div align="center">
  <h3>In-Depth Algorithm Analysis with Digit Buckets</h3>
  <h4>Comprehensive Study of Non-Comparative Integer Sorting</h4>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Algorithm-FF6B6B?style=for-the-badge" alt="Algorithm" />
  <img src="https://img.shields.io/badge/Team_Project-9C27B0?style=for-the-badge" alt="Team Project" />
  <img src="https://img.shields.io/badge/Academic-1E90FF?style=for-the-badge" alt="Academic" />
</div>

---

## Overview

A comprehensive academic project providing **in-depth analysis of Radix Sort** — one of the most efficient non-comparative integer sorting algorithms. This project covers the complete picture: algorithm mechanics, pseudocode, flowcharts, dry run examples, asymptotic analysis, and practical implementations in both **C++** and **Python**.

The project also features comparative studies against popular sorting algorithms like **Quick Sort** and **Merge Sort**, along with insights into real-world applications where Radix Sort excels.

---

## Project Highlights

- Complete algorithm explanation with pseudocode
- Detailed flowchart visualization
- Step-by-step dry run examples
- Asymptotic time and space complexity analysis
- Implementations in **two programming languages** (C++ and Python)
- Comparative analysis with Quick Sort and Merge Sort
- Real-world applications and optimal use cases
- Comprehensive documentation (Report + Presentations)
- Academic team project with collaborative effort

---

## What is Radix Sort?

**Radix Sort** is a non-comparative integer sorting algorithm that sorts numbers digit by digit, starting from the least significant digit (LSD) or most significant digit (MSD).

Unlike comparison-based algorithms (Quick Sort, Merge Sort), Radix Sort works by:

1. **Distributing** numbers into buckets based on individual digits
2. **Collecting** them in order
3. **Repeating** for each digit position

This approach makes it incredibly efficient for sorting integers with bounded digit counts.

---

## How It Works (Digit Bucket Method)

### Step-by-Step Process

```
1. Find the maximum number to determine digit count
2. For each digit position (units, tens, hundreds, ...):
   a. Create 10 buckets (0 through 9)
   b. Distribute numbers into buckets based on current digit
   c. Collect numbers from buckets in order (0 to 9)
3. After processing all digits, the array is sorted
```

### Visual Example

Sorting `[170, 45, 75, 90, 802, 24, 2, 66]`:

**Pass 1 (Units digit):**
```
Bucket 0: [170, 90]
Bucket 2: [802, 2]
Bucket 4: [24]
Bucket 5: [45, 75]
Bucket 6: [66]
Result: [170, 90, 802, 2, 24, 45, 75, 66]
```

**Pass 2 (Tens digit):**
```
Bucket 0: [802, 2]
Bucket 2: [24]
Bucket 4: [45]
Bucket 6: [66]
Bucket 7: [170, 75]
Bucket 9: [90]
Result: [802, 2, 24, 45, 66, 170, 75, 90]
```

**Pass 3 (Hundreds digit):**
```
Bucket 0: [2, 24, 45, 66, 75, 90]
Bucket 1: [170]
Bucket 8: [802]
Final Sorted: [2, 24, 45, 66, 75, 90, 170, 802]
```

---

## Time and Space Complexity

### Time Complexity

| Case | Complexity |
|------|------------|
| Best Case | O(n × k) |
| Average Case | O(n × k) |
| Worst Case | O(n × k) |

Where:
- `n` = number of elements
- `k` = number of digits in the largest number

### Space Complexity

| Aspect | Complexity |
|--------|------------|
| Auxiliary Space | O(n + b) |
| Total Space | O(n + b) |

Where:
- `b` = base of the number system (10 for decimal)

---

## Comparison with Other Sorting Algorithms

| Algorithm | Best Case | Average Case | Worst Case | Space | Comparative? |
|-----------|-----------|--------------|------------|-------|--------------|
| **Radix Sort** | O(nk) | O(nk) | O(nk) | O(n+b) | No |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |

### When Radix Sort Wins
- Sorting integers with limited digit count
- Large datasets with small key range
- When stable sorting is required
- When O(n log n) lower bound needs to be beaten

### When Other Algorithms Win
- Sorting floating-point numbers (Quick Sort, Merge Sort)
- Variable-length keys (Merge Sort)
- Memory-constrained systems (Insertion Sort)
- General-purpose sorting (Quick Sort)

---

## Tech Stack

**Programming Languages:**
- C++ — For high-performance implementation
- Python — For readable, educational implementation

**Documentation Tools:**
- Microsoft Word for detailed report
- Microsoft PowerPoint for presentation slides
- Markdown for repository documentation

---

## Project Structure

```
Radix-Sort-With-Digit-Buckets/
│
├── CODE.TXT                       # Implementation in C++ and Python
├── Report.docx                    # Comprehensive analysis report
├── radix bucket sort.pptx         # Detailed presentation slides
├── 3Minute.pptx                   # Quick 3-minute summary slides
└── README.md                      # Project documentation
```

---

## Implementation Highlights

### Python Implementation (Educational)
- Clear and readable code
- Step-by-step comments
- Easy to understand for learners
- Demonstrates algorithm logic

### C++ Implementation (Performance)
- Optimized for speed
- Memory-efficient bucket management
- Production-ready code style
- Performance benchmarking ready

Both implementations are available in the **CODE.TXT** file in the repository.

---

## Pseudocode

```
Algorithm RadixSort(array):
    max_num = findMax(array)
    
    for digit = 1 while max_num/digit > 0:
        buckets = createBuckets(10)
        
        for each number in array:
            digit_value = (number / digit) % 10
            place number in buckets[digit_value]
        
        index = 0
        for each bucket in buckets:
            for each number in bucket:
                array[index] = number
                index = index + 1
        
        digit = digit * 10
    
    return array
```

---

## Real-World Applications

### 1. Database Indexing
Radix Sort is used in database systems for sorting large integer keys efficiently.

### 2. Dictionary Sorting
Suffix arrays and trie data structures benefit from radix-based sorting.

### 3. Postal Code Sorting
Mail sorting machines use principles similar to Radix Sort for ZIP codes.

### 4. Network Routing
IP address sorting in routing tables uses radix-based approaches.

### 5. Computer Graphics
Sorting pixel data and color values for rendering optimizations.

### 6. Big Data Processing
Distributed sorting algorithms like MapReduce use radix-based partitioning.

### 7. Compiler Design
Symbol tables and lexical analysis benefit from fast integer sorting.

---

## Optimal Use Cases

Radix Sort is **best suited** when:

- All keys are integers (or can be represented as integers)
- The maximum number of digits is known and small
- Stability is required in sorting
- The dataset is large enough that O(nk) beats O(n log n)
- Memory is not a critical constraint

Radix Sort is **not suitable** when:

- Sorting floating-point numbers directly
- Keys have widely varying lengths
- Memory is highly constrained
- Sorting requires custom comparison logic

---

## Documentation

This project includes comprehensive documentation:

### 1. Report.docx
Full academic report covering:
- Algorithm theory and history
- Detailed mathematical analysis
- Step-by-step examples
- Comparative study with other algorithms
- Conclusions and recommendations

### 2. radix bucket sort.pptx
Complete presentation slides for in-depth study and academic presentation.

### 3. 3Minute.pptx
Condensed summary slides for quick overview and elevator pitch.

### 4. CODE.TXT
Working implementations in both C++ and Python with detailed comments.

---

## Installation and Usage

### Prerequisites

- C++ compiler (g++, clang, or MSVC)
- Python 3.6 or higher
- Text editor or IDE

### Running the C++ Implementation

```bash
git clone https://github.com/MuhammadYasir85a/Radix-Sort-With-Digit-Buckets.git
cd Radix-Sort-With-Digit-Buckets
```

Copy the C++ code from `CODE.TXT` into a file named `radix_sort.cpp`:

```bash
g++ radix_sort.cpp -o radix_sort
./radix_sort
```

### Running the Python Implementation

Copy the Python code from `CODE.TXT` into a file named `radix_sort.py`:

```bash
python radix_sort.py
```

---

## Learning Outcomes

Through this project, the team gained understanding of:

- Non-comparative sorting algorithm design
- Asymptotic complexity analysis
- Comparative algorithm evaluation
- Implementation in multiple languages
- Algorithm visualization and explanation
- Technical documentation and presentation
- Collaborative academic research

---

## Project Status

**Status:** Completed

All deliverables (code, report, presentations) are complete and available in the repository.

---

## Academic Information

| Field | Detail |
|-------|--------|
| Course | Data Structures and Algorithms |
| Institution | Namal University Mianwali |
| Instructor | Prof. Dr. Mudassar Raza |
| Project Type | Academic Team Project |

---

## Contributors

| Name | Role |
|------|------|
| **Muhammad Yasir** | Algorithm Implementation, Documentation |
| **Rehan Ali** | Algorithm Analysis, Presentation Design |
| **Ahmad Hassan** | Comparative Studies, Code Review |

---

## Author

**Muhammad Yasir**

Computer Science Undergraduate at Namal University Mianwali  
Aspiring AI and Computer Vision Engineer

<div>
  <a href="https://www.linkedin.com/in/muhammad-yasir-6a9500343/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:muhammadyasir85a@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://github.com/MuhammadYasir85a">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</div>

---

## Acknowledgments

- **Prof. Dr. Mudassar Raza** for excellent guidance throughout the project
- **Namal University Mianwali** for academic support and resources
- **Rehan Ali and Ahmad Hassan** for outstanding teamwork
- Computer science textbooks and academic papers on sorting algorithms

---

## References

- "Introduction to Algorithms" by Cormen, Leiserson, Rivest, and Stein
- "The Art of Computer Programming, Volume 3: Sorting and Searching" by Donald Knuth
- Academic papers on non-comparative sorting algorithms
- Online resources on algorithm complexity analysis

---

## License

This project is licensed under the **MIT License**.

This is an academic project. The code and documentation are freely available for educational purposes with proper attribution.

---

<div align="center">
  <i>"Sort smarter, not just faster — understanding algorithms beyond comparison."</i>
</div>

<br/>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=2ECC71&height=100&section=footer" width="100%" />
</div>
