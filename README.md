

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Stack:
    def __init__(self):
        self.top = None

    def push(self, data):
        new = Node(data)
        new.next = self.top
        self.top = new
        print(data, "pushed")

    def pop(self):
        if self.top is None:
            print("Stack is Empty")
        else:
            temp = self.top
            self.top = temp.next
            print(temp.data, "popped")

    def display(self):
        if self.top is None:
            print("Stack is Empty")
        else:
            temp = self.top
            print("Stack elements:")
            while temp:
                print(temp.data)
                temp = temp.next


# Example
s = Stack()
s.push(10)
s.push(20)
s.push(30)
s.display()
s.pop()
s.display()
