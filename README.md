import random
from datetime import datetime
def verificar_patente(patente):
    vocales="AEIOU"
    if len(patente)!=6:
        return 0
        if patente[:4].isalpha()and patente[:4].isdigit()and not any(v in patente[:4].upper()for v in vocales):
            return 1
    if patente[:2].isalpha() and patente [2:].isdigit()and not any(v in patente[:4].upper()for v in vocales):
        return 1
    return 0
    def grabar (datos,multa):
        registro=[]
        registro.append(datos["Tipo"])
        registro.append(datos["Patente"].upper())
        registro.append(datos["Marca"])
        registro.append(datos["Precio"])
        registro.append(datos["Dueño"])
        registro.append(datos["Fecha"])
        registro.append(multas)
        registro.append(random.radint(1500,3500))
        registro.append(random.radint(1500,3500))
        return registro 
    def buscar (patente,registro):
        patente=patente.upper()
        Nacho=0
        cont=1
        for x in registro:
            if patente==x[1]:
                Nacho=0
                print("Tipo",x[0])
                print("patente",x[1])
                print("Marca",x)
                print("Precio",x[3])
                print("Dueño",x[4])
                print("Fecha",x[5])
                if len(x[6])==0:
                    print("No se encontraron multas.")
                elif len(x[6])==1:
                    print("Se encontro 1 multa")
                else:
                    print("Se encontraron", len(x[6],"multas"))
                for multa in x[6]:
                    if len (multa)>0:
                        print("multa",cont)
                        print("monto",multa[0])
                        print("Fecha", multa[1])
                        cont+=1
        if lili==0:
            print("No se encontraron multas")
            return 0
    def certificados(patente,registros):
        patente=patente.upper()
        Nacho=0
        cont=1
        for x in registros:
            if patente==x[1]:
                Nacho=1
                print("\n")
                print("-----------------------------------------")
                print("Certificado de Emision de contaminantes")
                print("Patente",x[1])
                print("Dueño",x[4])
                print("Valor",x[7])
                print("  APROBRADO    ")
                print("\n")
                print("------------------------------------------")
                print("Certificado de Anotaciones vigentes")
                print("Patente",x[1])
                print("Dueño",x[4])
                print("Valor",x[8])
                print("  APROBRADO    ")
                if len(x[6])==0:
                    print("No se encontraron multas")
                elif len (x[6])==1:
                    print("Se encontro 1 multa")
                else:
                    print("Se encontraron",len(x[6]),"multas")
                    for multa in x[6]:
                        if len (multa)>0:
                            print("Multa",cont)
                            print("Monto",multa[0])
                            print("Fecha",multa[1])
                            cont+=1
                if Nacho==0:
                    print("No se encontraron resgitros ")
                    return 0
                registros =[]
                menu=0
                while menu!=4:
                    print("1.-Grabar")
                    print("2.-Buscar")
                    print("3.-Imprimir Certificados")
                    print("4.-Salir") 
                    menu=int(input("Escoja una alternativa: "))
                    if menu<1 or menu>4:
                        print("Opcion invalida")
                    if menu==1:
                        datos={"Tipo":"x","Patente":"x","Marca":"x","Precio":0,"Dueño":"x","Fecha":"x"}
                        multas=[]
                        pat=0
                        datos["Tipo"]=input("Ingrese tipo de vehículo: ")
                        while pat==0:
                            datos["Patente"]=input("Ingrese patente de vehículo: ")
                            pat=verificar_patente(datos["Patente"])
                            if pat==0:
                                print("Patente invalida")
                        while len(datos["Marca"])<2 or len(datos["Marca"])>15:
                            datos ["Marca"]=input("Ingrese marca de vehículo: ")
                            if len(datos["Marca"])<2 or len(datos["Marca"])>15:
                                print("La marca debe tener entre 2 a 15 caracteres")
                        while datos["Precio"]<5000000:
                            datos["Precio"]=int(input("Ingrese el valor del Vehículo"))
                            print("El precio debe ser mas de $5.000.000")
                        datos ["Dueño"]=int("Ingrese el nombre del dueño")
                        while True:
                            datos["Fecha"]=int("Ingrese la fecha de registro del vehículo (aaaa/mm/dd): ")
                            try:
                                fecha=datetime.strtime(datos["Fecha"],'%Y/%m/%D').strftime('%D-%m-%Y')
                                print("La fecha de registro del vehículo es: ")
                                print(str(fecha))
                                except ValueError:
                                    print("No ha ingresado una fecha correcta ")
                                else:
                                    break
            mult=int(input("¿Tiene multas?: 1.-Si 2.-No"))
                while mult==1:
                    multas2=[]
                    multas2.append(int(input("Ingrese el monto de la multa: ")))
                        while True:
                            multas2.append(int(input("Ingrese la fecha de la multa (aaaa/mm/dd): ")))
                            try:
                                fecha=datetime.strptime(multas2[-1]'%Y/%m/%D')strftime('%D-%m-%Y')
                                print("La fecha de la multa es: ")
                                print(str(fecha))
                                except ValueError:
                                    print("No ha ingresado una fecha correcta ")
                                else:
                                    break
                            multas.append(multas2)
                            mult=int(input("Tiene otra multa?"))

