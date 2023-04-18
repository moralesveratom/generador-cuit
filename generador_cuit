"""
Este archivo esta dedicado a la funcion de generacion de CUIT
"""

import random


def generador_cuit():

    def obtener_tipo():
        tipos = [20, 24, 27, 30, 34]
        selector_tipo = random.choice(tipos)

        return selector_tipo

    def obtener_dni():
        dni = (int(random.random() * 89999999 + 10000000))

        return dni

    def obtener_cuit():
        tipo = obtener_tipo()
        dni = obtener_dni()
        cuit = "{}{}".format(tipo, dni)

        return int(cuit)

    def calcular_verificador():
        cuit = obtener_cuit()
        suma = 0
        for i in range(len(str(cuit))):
            calculator = int(len(str(cuit)) - i - 1)
            suma += int(str(cuit)[calculator]) * (2 + (i % 6))

        verificador_calculator = (11 - (suma % 11))

        if verificador_calculator == 11:
            verificador_rest = verificador_calculator

            return verificador_rest
        else:
            verificador_rest = verificador_calculator
            return [cuit, verificador_rest]

    entire_value = calcular_verificador()
    cuit = entire_value[0]
    verification_code = entire_value[1]

    if entire_value[1] == 10:
        generador_cuit()
    else:
        return int(str(cuit) + str(verification_code))
