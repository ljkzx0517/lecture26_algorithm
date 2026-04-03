[04_python_최영진.ipynb](https://github.com/user-attachments/files/26456149/04_python_.ipynb)
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "820800eb-79fb-42d9-ad9c-8cabf6d7751d",
   "metadata": {},
   "outputs": [],
   "source": [
    "리스트 항목에 접근하기 : 슬라이싱(slicing)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "94766b3e-6198-448f-91ef-0e352f1da47d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1, 2, 3, 4, 5]\n",
      "[6, 7, 8]\n",
      "[2, 5, 8]\n",
      "[1, 3, 5]\n",
      "[1, 4, 7]\n",
      "[1, 2, 3, 4, 5, 6, 7, 8]\n",
      "[1, 2, 3, 4, 5, 6, 7, 8]\n",
      "[8, 6, 4]\n",
      "[2, 3, 4, 5, 6, 7]\n",
      "[6, 5, 4, 3, 2, 1]\n",
      "[8, 7, 6, 5, 4, 3, 2, 1]\n",
      "[1, 2, 3, 4, 5, 6, 7, 8]\n"
     ]
    }
   ],
   "source": [
    "test_list = [1, 2, 3, 4, 5, 6, 7, 8]\n",
    "\n",
    "print(test_list[:5])\n",
    "print(test_list[5:])\n",
    "\n",
    "print(test_list[1::3])\n",
    "print(test_list[:5:2])\n",
    "print(test_list[::3])\n",
    "print(test_list[:])\n",
    "print(test_list[::])\n",
    "\n",
    "print(test_list[-1:-7:-2])\n",
    "print(test_list[1:-1:])\n",
    "print(test_list[-3::-1])\n",
    "print(test_list[::-1])\n",
    "print(test_list[::])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "e7113300-eba3-4b0a-865c-5adb1fa2dbfb",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[3, 2, 1]\n"
     ]
    }
   ],
   "source": [
    "print([1, 2, 3][::-1])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "cb55550b-d089-4907-bbb3-9d3500495b37",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[111, 222, 333, 3, 4, 5, 6, 7, 8]\n"
     ]
    }
   ],
   "source": [
    "test_list = [1, 2, 3, 4, 5, 6, 7, 8]\n",
    "test_list[:2] = [111, 222, 333]\n",
    "print(test_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "ee9fdd36-f5a3-4346-b396-d6806c899bb4",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "원본 데이터 ['one', 'two', 'three', 'foer']\n",
      "역순 데이터 ['foer', 'three', 'two', 'one']\n",
      "정렬 후 데이터 ['foer', 'one', 'three', 'two']\n",
      "원본 데이터 ['four', 'one', 'three', 'two']\n",
      "정렬 후 데이터 ['four', 'one', 'three', 'two']\n",
      "['one', 'two', 'four', 'three']\n"
     ]
    }
   ],
   "source": [
    "a_list = ['one', 'two', 'three', 'foer']\n",
    "print('원본 데이터', a_list)\n",
    "a_list.reverse()\n",
    "print('역순 데이터',a_list)\n",
    "\n",
    "a_list.sort()\n",
    "print('정렬 후 데이터',a_list)\n",
    "\n",
    "a_list = ['one', 'two', 'three', 'four']\n",
    "a_list = sorted(a_list)\n",
    "print('원본 데이터', a_list)\n",
    "print('정렬 후 데이터', a_list)\n",
    "\n",
    "c_list = sorted(a_list, key=len)\n",
    "print(c_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "d14dc539-1a68-4888-880a-71aab09b434d",
   "metadata": {},
   "outputs": [],
   "source": [
    "scores = [95, 45, 21, 74, 55]\n",
    "print(sorted(scores, reverse=True))\n",
    "\n",
    "print(scores)\n",
    "scores.sort(reverse=True)\n",
    "print(scores)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "0f7cb3be-77cd-4f31-8538-e2a8c835bfba",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "숫자 : 5\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1, 2, 3, 4, 5]\n"
     ]
    }
   ],
   "source": [
    "# 1 ~ N의 수로 이루어진 리스트 생성\n",
    "N = int(input(\"숫자 :\"))\n",
    "num_list =[]\n",
    "for i in range(1,N+1):\n",
    "    num_list.append(i)\n",
    "print(num_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "9dcc8877-b4af-4a72-8a77-c4077462b248",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "숫자 : 10\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]\n",
      "[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "숫자 : 10\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]\n"
     ]
    }
   ],
   "source": [
    "# 1 ~ N의 수로 이루어진 리스트 생성\n",
    "N = int(input(\"숫자 :\"))\n",
    "num_list =[i for i in range(1,N+1)]\n",
    "print(num_list)\n",
    "\n",
    "# expressoon\n",
    "num_list = [i * 2 for i in range(1,N+1)]\n",
    "print(num_list)\n",
    "\n",
    "# if문 사용\n",
    "N = int(input(\"숫자 :\"))\n",
    "NUM_list = [i for i in range(1,N+1) if i % 2 == 0]\n",
    "print(num_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "df1179fe-66f8-4714-ab8c-8fd5d9cc538d",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "4\n",
      "78\n",
      "11\n",
      "3\n",
      "274\n"
     ]
    }
   ],
   "source": [
    "# 1. 특정 값의 index 찾기\n",
    "def getIndex(num_list, target):\n",
    "    for i in range(len(num_list)):\n",
    "        if num_list[i] == target:\n",
    "            return i\n",
    "    return -1  # 없을 경우\n",
    "\n",
    "\n",
    "# 2. 최대값 반환\n",
    "def getMax(num_list):\n",
    "    max_val = num_list[0]\n",
    "    for num in num_list:\n",
    "        if num > max_val:\n",
    "            max_val = num\n",
    "    return max_val\n",
    "\n",
    "\n",
    "# 3. 최소값 반환\n",
    "def getMin(num_list):\n",
    "    min_val = num_list[0]\n",
    "    for num in num_list:\n",
    "        if num < min_val:\n",
    "            min_val = num\n",
    "    return min_val\n",
    "\n",
    "\n",
    "# 4. target보다 큰 값 개수 세기\n",
    "def countGT(num_list, target):\n",
    "    count = 0\n",
    "    for num in num_list:\n",
    "        if num > target:\n",
    "            count += 1\n",
    "    return count\n",
    "\n",
    "\n",
    "# 5. 전체 합\n",
    "def sumList(num_list):\n",
    "    total = 0\n",
    "    for num in num_list:\n",
    "        total += num\n",
    "    return total\n",
    "\n",
    "\n",
    "# 6. 리스트 뒤집기 (swap)\n",
    "def swapList(num_list):\n",
    "    left = 0\n",
    "    right = len(num_list) - 1\n",
    "    \n",
    "    while left < right:\n",
    "        num_list[left], num_list[right] = num_list[right], num_list[left]\n",
    "        left += 1\n",
    "        right -= 1\n",
    "\n",
    "\n",
    "# 테스트\n",
    "number_list = [23, 45, 27, 11, 25, 65, 78]\n",
    "\n",
    "print(getIndex(number_list, 25))\n",
    "print(getMax(number_list))         \n",
    "print(getMin(number_list))         \n",
    "print(countGT(number_list, 42)) \n",
    "print(sumList(number_list))"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python [conda env:base] *",
   "language": "python",
   "name": "conda-base-py"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.13.9"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
