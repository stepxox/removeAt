#include <stdio.h>
#include <malloc.h>
#include <string.h>

void removeAt(int **array, int size, int index) {
    int realSize = size - 1;
    int *tmp = malloc(realSize * sizeof(int));
    // zkopirovani prvku pred zadanym indexem
    if (index != 0) {
        memcpy(tmp, *array, index * sizeof(int));
    }
    if (index != realSize) {
        memcpy(tmp + index, (*array) + index + 1, (realSize - index) * sizeof(int));
    }
    free(*array);
    *array = tmp;
}

int main(void) {
    int n = 10;
    int a;
    int *ptr = (int*) malloc(n * sizeof(int));

    for (int i = 0; i < n; i++) {
        ptr[i] = i + 1;
        printf("%d ", ptr[i]);
    }

    printf("\n");
    a = getchar() - '0';
    //scanf("%d", &a);

    removeAt(&ptr, n, a);
    n--;
    for (int i = 0; i < n; i++) {
        printf("%d ", ptr[i]);
    }
    printf("\n");

    free(ptr);
    ptr = NULL;
    return 0;
}
