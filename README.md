# Working-with-Collections-and-Functions
Python Basics
# =====================================================
# Python Assignment
# Topics: Tuples, Lists, Sets, and Functions
# This script completes all required tasks.
# =====================================================


# =====================================================
# Part 1: Tuples
# =====================================================

# 1. Create and Access

# Define a tuple with at least 5 numerical values
numbers_tuple = (10, 20, 30, 40, 50)

# Print the third item in the tuple
# Index 2 represents the third position
print("1b. Third item in tuple:", numbers_tuple[2])


# 2. Tuple Modification (Workaround)

# Since tuples are immutable, convert the tuple to a list
tuple_to_list = list(numbers_tuple)

# Remove an item from the list
tuple_to_list.remove(30)

# Convert the list back to a tuple
modified_tuple = tuple(tuple_to_list)

# Print the modified tuple
print("2a. Modified tuple after removing an item:", modified_tuple)


# 3. Tuple Unpacking

# Create a tuple with values to unpack
person_info = ("Lavenda", 21, "Kenya")

# Unpack tuple values into individual variables
name, age, country = person_info

# Print each unpacked variable
print("3a. Name:", name)
print("3a. Age:", age)
print("3a. Country:", country)


# 4. Tuple to String

# Create a tuple of characters
char_tuple = ('P', 'Y', 'T', 'H', 'O', 'N')

# Join the characters into a single string
word = ''.join(char_tuple)

# Print the resulting string
print("4a. Tuple converted to string:", word)


# 5. Find Duplicates

# Create a tuple with repeated elements
duplicate_tuple = (1, 2, 3, 2, 4, 5, 1, 6, 3)

# Create an empty list to store duplicate values
duplicates = []

# Loop through each item in the tuple
for item in duplicate_tuple:

    # Check if item appears more than once and is not already added
    if duplicate_tuple.count(item) > 1 and item not in duplicates:
        duplicates.append(item)

# Print duplicate values
print("5a. Duplicate values:", duplicates)


# 6. Reverse Tuple

# Reverse the tuple using slicing
reversed_tuple = numbers_tuple[::-1]

# Print the reversed tuple
print("6a. Reversed tuple:", reversed_tuple)


# =====================================================
# Part 2: Lists
# =====================================================

# 7. Sum of List

# Create a list of numbers
number_list = [5, 10, 15, 20, 25]

# Calculate the sum of all items in the list
total = sum(number_list)

# Print the total sum
print("7a. Sum of list items:", total)


# 8. Remove Duplicates

# Create a list containing duplicate values
duplicate_list = [1, 2, 2, 3, 4, 4, 5, 1]

# Create an empty list to store unique values
unique_list = []

# Loop through the list
for item in duplicate_list:

    # Add item only if it does not already exist
    if item not in unique_list:
        unique_list.append(item)

# Print list without duplicates
print("8a. List without duplicates:", unique_list)


# 9. Clone a List

# Create the original list
original_list = [10, 20, 30, 40]

# Method 1: Copy using slicing
copy1 = original_list[:]

# Method 2: Copy using list() function
copy2 = list(original_list)

# Method 3: Copy using copy() method
copy3 = original_list.copy()

# Print all copied lists
print("9a. Original list:", original_list)
print("9a. Copy using slicing:", copy1)
print("9a. Copy using list():", copy2)
print("9a. Copy using copy():", copy3)


# 10. Combine Lists

# Create two separate lists
list1 = [1, 2, 3]
list2 = [4, 5, 6]

# Combine both lists
combined_list = list1 + list2

# Print the combined list
print("10a. Combined list:", combined_list)


# 11. Sort by Last Element in Tuple

# Create a list of non-empty tuples
tuple_list = [(2, 5), (1, 2), (4, 1), (3, 7)]

# Sort tuples based on the last element
sorted_tuples = sorted(tuple_list, key=lambda x: x[-1])

# Print sorted tuples
print("11a. Sorted tuples:", sorted_tuples)


# 12. List Slicing

# Create a list with names of 10 people
people_names = [
    "Alice", "Bob", "Charlie", "David", "Eva",
    "Frank", "Grace", "Hannah", "Ian", "Jack"
]

# Use slicing to print the first 4 names
print("12a. First 4 names:", people_names[:4])


# =====================================================
# Part 3: Sets
# =====================================================

# 13. Create a Set

# Create a set with at least 5 elements
my_set = {10, 20, 30, 40, 50}

# Print the set
print("13a. Set elements:", my_set)


# 14. Set Intersection

# Create two sets with common elements
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}

# Find common elements using intersection
common_elements = set1.intersection(set2)

# Print intersection
print("14a. Intersection of sets:", common_elements)


# 15. Set Union

# Find union of the two sets
union_set = set1.union(set2)

# Print union
print("15a. Union of sets:", union_set)


# =====================================================
# Part 4: Functions
# =====================================================

# 16. Multiply List Elements

# Define a function to multiply all numbers in a list
def multiply_list(numbers):

    # Start with 1 because multiplying by 0 gives 0
    product = 1

    # Multiply each number in the list
    for number in numbers:
        product *= number

    # Return the final product
    return product


# Create a sample list of numbers
numbers = [2, 3, 4, 5]

# Call the function and print result
print("16a. Product of list items:", multiply_list(numbers))


# 17. Statistics Function

# Generate a list of test scores
test_scores = [85, 90, 78, 92, 88, 76, 95]

# Define a function to calculate minimum, maximum, and average
def calculate_statistics(scores):

    # Find minimum score
    minimum = min(scores)

    # Find maximum score
    maximum = max(scores)

    # Calculate average score
    average = sum(scores) / len(scores)

    # Return all three values
    return minimum, maximum, average


# Call the function and store returned values
min_score, max_score, avg_score = calculate_statistics(test_scores)

# Print statistics
print("17b. Minimum score:", min_score)
print("17b. Maximum score:", max_score)
print("17b. Average score:", avg_score)


# 18. Check Range Membership

# Define a function to check if a number is within a range
def check_range(number, start, end):

    # Return True if number is within range, otherwise False
    return start <= number <= end


# Test the function
print("18a. Is 15 within range 10 to 20?",
      check_range(15, 10, 20))


# 19. Dog Speed Analyzer

# Create a nested list with dog breeds and max speeds
dogs = [
    ["Greyhound", 45],
    ["German Shepherd", 30],
    ["Labrador Retriever", 20],
    ["Jack Russell Terrier", 25],
    ["Whippet", 35]
]

# Define a function to find the fastest and slowest dog
def dog_speed_analyzer(dog_list):

    # Find the dog with maximum speed
    fastest = max(dog_list, key=lambda dog: dog[1])

    # Find the dog with minimum speed
    slowest = min(dog_list, key=lambda dog: dog[1])

    # Return both dogs
    return fastest, slowest


# Call the function
fastest_dog, slowest_dog = dog_speed_analyzer(dogs)

# Print results
print("19b. Fastest dog:", fastest_dog)
print("19b. Slowest dog:", slowest_dog)
