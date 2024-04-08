# Listmanipulator
# Define the ListManipulator class
class ListManipulator:
    def __init__(self):
        self.internal_list = []

    def add_elements(self, elements):
        self.internal_list.extend(elements)

    def remove_duplicates(self):
        self.internal_list = list(set(self.internal_list))

    def reverse_list(self):
        self.internal_list.reverse()

    def sort_list(self):
        self.internal_list.sort()

    def get_unique_elements(self):
        return list(set(self.internal_list))

    def remove_element(self, element):
        if element in self.internal_list:
            self.internal_list.remove(element)

    def get_list(self):
        return self.internal_list

# Example usage of the ListManipulator class
if __name__ == "__main__":
    # Create an instance of ListManipulator
    manipulator = ListManipulator()

    # Add elements to the list
    manipulator.add_elements([1, 2, 3, 4, 3, 2, 1])
    print("List after adding elements:", manipulator.get_list())

    # Remove duplicates
    manipulator.remove_duplicates()
    print("List after removing duplicates:", manipulator.get_list())

    # Reverse the list
    manipulator.reverse_list()
    print("List after reversing:", manipulator.get_list())

    # Sort the list
    manipulator.sort_list()
    print("List after sorting:", manipulator.get_list())

    # Get unique elements
    unique_elements = manipulator.get_unique_elements()
    print("Unique elements:", unique_elements)

    # Remove an element
    manipulator.remove_element(2)
    print("List after removing element 2:", manipulator.get_list())

