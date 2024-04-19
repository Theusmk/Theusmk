class BichoVirtual:
    def __init__(self, nome):
        self.nome = nome
        self.fome = 50
        self.saude = 50
        self.felicidade = 50

    def alimentar(self):
        self.fome -= 10
        self.saude += 5
        self.felicidade += 2
        print("Você alimentou o seu bicho virtual.")

    def brincar(self):
        self.fome += 5
        self.saude += 2
        self.felicidade -= 10
        print("Você brincou com o seu bicho virtual.")

    def dormir(self):
        self.fome += 2
        self.saude += 10
        self.felicidade += 5
        print("Você deixou o seu bicho virtual dormir.")

    def mostrar_status(self):
        print("\nStatus do Bicho Virtual:")
        print("Nome:", self.nome)
        print("Fome:", self.fome)
        print("Saúde:", self.saude)
        print("Felicidade:", self.felicidade)

def main():
    nome_bicho = input("Escolha um nome para o seu bicho virtual: ")
    bicho = BichoVirtual(nome_bicho)
    while True:
        print("\nO que você deseja fazer?")
        print("1 - Alimentar")
        print("2 - Brincar")
        print("3 - Deixar dormir")
        print("4 - Mostrar status")
        print("5 - Sair do jogo")

        escolha = input("Escolha uma opção: ")

        if escolha == "1":
            bicho.alimentar()
        elif escolha == "2":
            bicho.brincar()
        elif escolha == "3":
            bicho.dormir()
        elif escolha == "4":
            bicho.mostrar_status()
        elif escolha == "5":
            print("Obrigado por jogar!")
            break
        else:
            print("Opção inválida. Escolha novamente.")

        # Atualiza o estado do bicho virtual a cada ação
        time.sleep(1)

if __name__ == "__main__":
    main()
