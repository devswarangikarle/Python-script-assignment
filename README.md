# Python-script-assignment
Raj's teacher has assigned him N tasks to finish within M days. Each task i takes Raj Ai days to complete, and he cannot work on multiple tasks simultaneously. Determine the maximum number of days Raj will have left for holiday activities if he successfully completes all the assignments. 

def maximum_days_left(M, N, assignments):
    assignments.sort()

    days_left = M
    for assignment in assignments:
        days_left -= assignment

        if days_left < 0:
            return -1

    return days_left

M, N = map(int, input().split())
assignments = list(map(int, input().split()))

result = maximum_days_left(M, N, assignments)
print(result)
