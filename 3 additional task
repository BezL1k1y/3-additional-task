A = [(16, 12, 19),
     (12, 50, 16),
     (17, 14, 91)]
B = [715,
     898,
     1190]
C = [9,
     13,
     8]
X = []


def matrix_check(matrix):
    matrix_check_len = len(matrix)
    check_sum = 0
    for i in range(matrix_check_len):
        check_sum += len(matrix[i])
    if check_sum / matrix_check_len == matrix_check_len:
        return True
    else:
        return False


def vector_multi_vector(vector1, vector2):
    vector1_len = len(vector1)
    vector2_len = len(vector2)
    vector_multi = 0
    if vector1_len == vector2_len:
        for i in range(vector1_len):
            vector_multi += vector1[i] * vector2[i]
    return vector_multi


def matrix_multi_vector(matrix, vector):
    matrix_len = len(matrix)
    vector_len = len(vector)
    vector_multi = []
    for i in range(vector_len):
        vector_multi.append(0)
    if matrix_check(matrix) and (matrix_len == vector_len):
        for i in range(matrix_len):
            for j in range(matrix_len):
                vector_multi[i] += matrix[i][j] * vector[j]
        return vector_multi
    else:
        return 0


def priority_index(vector):
    index_list = []
    vector_len = len(vector)
    Vector = sorted(vector, reverse=True)
    for i in range(vector_len):
        index_list.append(vector.index(Vector[i]))
    return index_list


def X_find(matrix, vector1, vector2):
    matrix_len = len(matrix)
    vector_len = len(vector1)
    vectorX = []
    for i in range(matrix_len):
        vectorX.append(0)
    if matrix_check(matrix) and (matrix_len == vector_len):
        for i in priority_index(vector2):
            stop = 0
            while stop != 1:
                vectorX[i] += 1
                if matrix_multi_vector(matrix, vectorX)[i] > vector1[i]:
                    stop = 1
                    vectorX[i] -= 1
    return vectorX


print(X_find(A, B, C))
print(vector_multi_vector(X_find(A, B, C), C))
