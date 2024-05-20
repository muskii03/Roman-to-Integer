# Roman-to-Integer
class Solution(object):

    def romanToInt(self, s):
        Roman_Values={
            "I":1,
            "V":5,
            "X":10,
            "L":50,
            "C":100,
            "D":500,
            "M":1000
            }
        total=0
        prev_value=0

        for char in s:
            value=Roman_Values[char]
            total+=value
            if value > prev_value:
                total-=2*prev_value
            prev_value=value

        return total
