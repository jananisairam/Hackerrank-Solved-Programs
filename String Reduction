from collections import deque

def stringReduction(a):
    queue = deque([a])
    min_length = len(a)
    while queue:
        a = queue.popleft()
        if len(a) < min_length:
            min_length = len(a)
        for i in range(len(a)-1):
            substring = a[i:(i+2)]
            if substring == "ab" or substring == "ba":
                queue.append(a[:i] + "c" + a[(i+2):])
            elif substring == "bc" or substring == "cb":
                queue.append(a[:i] + "a" + a[(i+2):])
            elif substring == "ac" or substring == "ca":
                queue.append(a[:i] + "b" + a[(i+2):])
    return min_length

