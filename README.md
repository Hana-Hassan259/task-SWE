import unittest
from calculator import calculator 
class Testcalculator(unittest.TestCase):
    def setUp(self):
        self.calc=calculator()
    
    def testadd(self):
        result= self.calc.add(3,7)
        self.assertEqual(result,10)

    def testadd(self):
        result= self.calc.add(-1,1)
        self.assertEqual(result,0)

    def testadd(self):
        result= self.calc.add(-1,-1)
        self.assertEqual(result,-2)

    
    def testsub(self):
        result= self.calc.subtract(10,5)
        self.assertEqual(result,5)

    def testsub(self):
        result= self.calc.subtract(-1,-1)
        self.assertEqual(result,0)

    def testmultibly(self):
        result=self.calc.multiply(-1,1)
        self.assertEqual(result,-1)

    def testdiv(self):
        result=self.calc.divide(10.5)
        self.assertEqual(result,2)

        with self.assertRaises(ValueError):
            self.calc.divide(10,0)

if __name__== "__main__":
    unittest.main()





    