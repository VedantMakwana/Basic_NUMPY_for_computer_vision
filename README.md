{
 "cells": [
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h1> Numpy"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 224,
   "metadata": {},
   "outputs": [],
   "source": [
    "import numpy as np"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->1D array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 225,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 225,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "arr_horrizontal = np.array([1,2,3])\n",
    "arr_horrizontal"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 226,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1],\n",
       "       [2],\n",
       "       [3]])"
      ]
     },
     "execution_count": 226,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "arr_vertical = np.array([[1],[2],[3]])\n",
    "arr_vertical\n",
    "\n"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->2D array "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 227,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1, 2, 3],\n",
       "       [3, 2, 4]])"
      ]
     },
     "execution_count": 227,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# we pass rows as tuples\n",
    "arr_2d = np.array([(1,2,3),(3,2,4)])\n",
    "arr_2d"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->3d array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 228,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[1, 2, 3],\n",
       "        [3, 2, 4]],\n",
       "\n",
       "       [[1, 2, 3],\n",
       "        [3, 2, 4]]])"
      ]
     },
     "execution_count": 228,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "arr_3d = np.array([[(1,2,3),(3,2,4)],[(1,2,3),(3,2,4)]])\n",
    "arr_3d"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->Different Arrays "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 229,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[0, 0, 0],\n",
       "       [0, 0, 0],\n",
       "       [0, 0, 0]], dtype=int8)"
      ]
     },
     "execution_count": 229,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# 2d arrays of all zeros with dimenssion (3,3)\n",
    "# dtype setting datatype of array\n",
    "arr_zero = np.zeros((3,3), dtype=np.int8)\n",
    "arr_zero"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 230,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1., 1., 1.],\n",
       "       [1., 1., 1.],\n",
       "       [1., 1., 1.]])"
      ]
     },
     "execution_count": 230,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# array of all ones\n",
    "arr_ones = np.ones((3,3))\n",
    "arr_ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 231,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[5, 5, 5],\n",
       "       [5, 5, 5],\n",
       "       [5, 5, 5]])"
      ]
     },
     "execution_count": 231,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# array of particular intiger \n",
    "# used in convolution \n",
    "arr_full = np.full((3,3),5)\n",
    "arr_full"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 232,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1., 0., 0.],\n",
       "       [0., 1., 0.],\n",
       "       [0., 0., 1.]])"
      ]
     },
     "execution_count": 232,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# identity Matrix \n",
    "arr_I= np.eye(3)\n",
    "arr_I"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->Random and Ranged array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 233,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])"
      ]
     },
     "execution_count": 233,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Array of vale range from 0 to 9 with gap of 1\n",
    "arr_range = np.arange(0,10,1)\n",
    "arr_range"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 234,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0.  , 0.25, 0.5 , 0.75, 1.  , 1.25, 1.5 , 1.75, 2.  ])"
      ]
     },
     "execution_count": 234,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Array of 9 element in range 0 to 2 \n",
    "arr_ls = np.linspace(0,2,9)\n",
    "arr_ls"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 235,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 4744.32811471, 51702.0316144 , 57334.63391409],\n",
       "       [18065.32869211, 60952.55505492, 17077.34831561]])"
      ]
     },
     "execution_count": 235,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Use to genrate noice in array\n",
    "# array of random no between 0,1 is genration \n",
    "arr_RandomFloat = np.random.rand(2,3)\n",
    "\n",
    "# scaling the above array \n",
    "arr_RandomFloat = arr_random*255\n",
    "\n",
    "arr_RandomFloat\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 236,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1, 2, 1],\n",
       "       [1, 3, 1],\n",
       "       [2, 1, 2]])"
      ]
     },
     "execution_count": 236,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Array of random intigers ranginf from 0 to 4\n",
    "# mostly use for adding inpurity\n",
    "arr_RandomIntiger = np.random.randint(5,size=(3,3))\n",
    "arr_RandomIntiger"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->Array inspection"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h4> 0) shape\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 237,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n",
      "shape of array (2, 3)\n"
     ]
    }
   ],
   "source": [
    "# Shape of an array \n",
    "# calculating hieght and width of an image \n",
    "# hight = image.shape[0] \n",
    "# width = image.shape[1]\n",
    "# segments = image.shape[2]\n",
    "print(arr_2d)\n",
    "shape =arr_2d.shape\n",
    "print(f\"shape of array {shape}\")"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "in above inspection 2 is no of rows and 3 is no of columns"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>1) Size"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 238,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n",
      "array have 6\n"
     ]
    }
   ],
   "source": [
    "# Calculating no of element in array \n",
    "# Use to calculate no of pixel in image\n",
    "print(arr_2d)\n",
    "no_of_element = arr_2d.size\n",
    "print(f\"array have {no_of_element}\")"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>2) Data Type"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 239,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "data type of array is 'int32'\n"
     ]
    }
   ],
   "source": [
    "data_type = arr_2d.dtype\n",
    "print(f\"data type of array is '{data_type}'\")"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>3) Min/Max/Mean/Std"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 240,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n",
      "min of array 1\n",
      "max of array 4\n",
      "Avg of array 2.5\n",
      "Std of array 0.96\n"
     ]
    }
   ],
   "source": [
    "print(arr_2d)\n",
    "print(f\"min of array {arr_2d.min()}\")\n",
    "print(f\"max of array {arr_2d.max()}\")\n",
    "print(f\"Avg of array {arr_2d.mean()}\")\n",
    "print(\"Std of array %.2f\"%arr_2d.std())"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>4) Changing Datatype of array "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 241,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "int32 \n",
      "\n",
      "[[1. 2. 3.]\n",
      " [3. 2. 4.]]\n",
      "float64\n"
     ]
    }
   ],
   "source": [
    "print(arr_2d.dtype,\"\\n\")\n",
    "\n",
    "# changing data type\n",
    "arr_2d_float = arr_2d.astype(float)\n",
    "print(arr_2d_float)\n",
    "print(arr_2d_float.dtype)"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->Basic math operation"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 242,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "array1\n",
      "[[0 1 2]\n",
      " [4 5 1]\n",
      " [1 5 2]]\n",
      "\n",
      "array2\n",
      "[[5 3 2]\n",
      " [0 1 3]\n",
      " [5 5 5]]\n",
      "\n"
     ]
    }
   ],
   "source": [
    "# Use for incresing Brightness , Contrast ,etc of an image\n",
    "arr1 = np.random.randint(6,size=(3,3))\n",
    "arr2 = np.random.randint(6,size=(3,3))\n",
    "\n",
    "print(f\"array1\\n{arr1}\\n\\narray2\\n{arr2}\\n\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 243,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "array addition\n",
      "[[ 5  4  4]\n",
      " [ 4  6  4]\n",
      " [ 6 10  7]]\n",
      "\n",
      "array subtraction \n",
      "[[-5 -2  0]\n",
      " [ 4  4 -2]\n",
      " [-4  0 -3]]\n",
      "\n",
      "array multiplication \n",
      "[[ 0  3  4]\n",
      " [ 0  5  3]\n",
      " [ 5 25 10]]\n"
     ]
    }
   ],
   "source": [
    "# perform element wise operation \n",
    "# addition \n",
    "arr_add = arr1+arr2\n",
    "print(f\"array addition\\n{arr_add}\\n\")\n",
    "\n",
    "# subtraction\n",
    "arr_sub = arr1-arr2\n",
    "print(f\"array subtraction \\n{arr_sub}\\n\")\n",
    "\n",
    "# multiplication\n",
    "arr_mult = arr1*arr2\n",
    "print(f\"array multiplication \\n{arr_mult}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 244,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[25 24 24]\n",
      " [24 26 24]\n",
      " [26 30 27]]\n"
     ]
    }
   ],
   "source": [
    "# Perfroming operation with simgle intiger\n",
    "print(arr_add + 20)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 245,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[-6 -3 -1]\n",
      " [ 3  3 -3]\n",
      " [-5 -1 -4]]\n"
     ]
    }
   ],
   "source": [
    "print(arr_sub-1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 246,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[ 0  6  8]\n",
      " [ 0 10  6]\n",
      " [10 50 20]]\n"
     ]
    }
   ],
   "source": [
    "print(arr_mult*2)"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h3>->Operation on image"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 247,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n",
      "(2, 3)\n"
     ]
    }
   ],
   "source": [
    "print(arr_2d)\n",
    "print(arr_2d.shape)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 248,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "4\n"
     ]
    }
   ],
   "source": [
    "# slecting an element of array\n",
    "x=1 #row ranging from 0-1\n",
    "y=2 #column ranging from 0-2\n",
    "print(arr_2d[x][y])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 249,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1 2 3]\n",
      "[1 2 3]\n"
     ]
    }
   ],
   "source": [
    "# selecting 1 row \n",
    "row = 0 #row to select\n",
    "print(arr_2d[row])\n",
    "# or\n",
    "print(arr_2d[row,:])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 250,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[2 2]\n"
     ]
    }
   ],
   "source": [
    "# Selecting Columns \n",
    "col = 1 \n",
    "print(arr_2d[:,col])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 251,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2]\n",
      " [3 2]]\n"
     ]
    }
   ],
   "source": [
    "# slicing \n",
    "\n",
    "print(arr_2d[:, 0:2])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 252,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]] \n",
      "\n",
      "Reversed\n",
      " [[3 2 4]\n",
      " [1 2 3]]\n"
     ]
    }
   ],
   "source": [
    "# Revercing columns array \n",
    "print(arr_2d,\"\\n\")\n",
    "\n",
    "print(\"Reversed\\n\" ,arr_2d[::-1])"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>->Reshape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 253,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n"
     ]
    }
   ],
   "source": [
    "# no of element should be contant while reshaping\n",
    "# Row*Column should always constant\n",
    "print(arr_2d)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 254,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3 3 2 4]]\n"
     ]
    }
   ],
   "source": [
    "# converting into 1d array\n",
    "reshaped_array = arr_2d.reshape(1,6)\n",
    "print(reshaped_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 255,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2]\n",
      " [3 3]\n",
      " [2 4]]\n"
     ]
    }
   ],
   "source": [
    "# converting in array with 3 rows and 2 columns \n",
    "reshaped_array= arr_2d.reshape(3,2)\n",
    "print(reshaped_array)"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>->Append \n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 256,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1 2 3 5 6 7]\n"
     ]
    }
   ],
   "source": [
    "# applied on 1d array only\n",
    "arr_1d = np.array([1,2,3,5,6,7])\n",
    "print(arr_1d)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 257,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[ 1  2  3  5  6  7 30]\n"
     ]
    }
   ],
   "source": [
    "# append \n",
    "arr_1d = np.append(arr_1d,30)\n",
    "print(arr_1d)\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 258,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1 2 3 5 6 7]\n"
     ]
    }
   ],
   "source": [
    "# delete\n",
    "arr_1d = np.delete(arr_1d,6)\n",
    "print(arr_1d)"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>->Flatening"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 259,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n"
     ]
    }
   ],
   "source": [
    "# converting array into vector\n",
    "# mostly use for image processing \n",
    "# there is diffrence between ravel and reshaping \n",
    "print(arr_2d)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 260,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1 2 3 3 2 4]\n"
     ]
    }
   ],
   "source": [
    "flattend_array = arr_2d.ravel()\n",
    "print(flattend_array)"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>->Concatenate \n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 261,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3, 5, 6, 7])"
      ]
     },
     "execution_count": 261,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "arr_1d"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 262,
   "metadata": {},
   "outputs": [],
   "source": [
    "arr_1d_2 =np.array([0,2,3,4])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 263,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[1 2 3 5 6 7 0 2 3 4]\n"
     ]
    }
   ],
   "source": [
    "print(np.concatenate((arr_1d,arr_1d_2)))"
   ]
  },
  {
   "attachments": {},
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<h5>->Transpose"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 264,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "[[1 2 3]\n",
      " [3 2 4]]\n",
      "[[1 3]\n",
      " [2 2]\n",
      " [3 4]]\n"
     ]
    }
   ],
   "source": [
    "print(arr_2d)\n",
    "print(arr_2d.transpose())"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
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
   "version": "3.11.3"
  },
  "orig_nbformat": 4
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
