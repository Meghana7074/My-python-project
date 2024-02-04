# math_utils.py

class MathUtils:
    @staticmethod
    def add(a, b):
        return a + b

    @staticmethod
    def subtract(a, b):
        return a - b

    @staticmethod
    def multiply(a, b):
        return a * b

    @staticmethod
    def divide(a, b):
        if b == 0:
            return -1.0
        return a / b
# test_math_utils.py
import pytest
from math_utils import MathUtils

@pytest.fixture
def math_utils_instance():
    return MathUtils()

def test_add(math_utils_instance):
    assert math_utils_instance.add(2, 3) == 5
    assert math_utils_instance.add(-2, 3) == 1

def test_subtract(math_utils_instance):
    assert math_utils_instance.subtract(5, 2) == 3
    assert math_utils_instance.subtract(2, 5) == -3

def test_multiply(math_utils_instance):
    assert math_utils_instance.multiply(2, 3) == 6
    assert math_utils_instance.multiply(-2, 3) == -6

def test_divide(math_utils_instance):
    assert math_utils_instance.divide(6, 3) == 2
    assert math_utils_instance.divide(5, 2) == 2.5

def test_divide_by_zero(math_utils_instance):
    assert math_utils_instance.divide(10, 0) == -1.0
# My-python-project
