class Veiculo:
    def calcular_custo(self, distancia):
        pass

class Carro(Veiculo):
    def calcular_custo(self, distancia):
        return distancia * 0.50

class Bicicleta(Veiculo):
    def calcular_custo(self, distancia):
        return 0

class Caminhao(Veiculo):
    def calcular_custo(self, distancia):
        return distancia * 1.20

def custo_total_viagem(veiculos):
    total = 0
    for veiculo in veiculos:
        total += veiculo.calcular_custo(200)
    return total

# Exemplo de uso
veiculos = [Carro(), Bicicleta(), Caminhao()]
print("Custo total:", custo_total_viagem(veiculos))
