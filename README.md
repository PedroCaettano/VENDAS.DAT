# VENDAS.DAT
Anotações de código presente em sala de aula

#include <iostream>
#include <stdio.h>
#include <fstream>
#include <cstring>

using namespace: std; 

struct Vendedor {
    int nomeVendedor:
    int codigo;
    char nome[50];
    double valorVenda;
    int mes;
};

int main () {
    nome_vendedor[2];

void criarArquivo() {
    std::ofstream arquivo("VENDAS.DAT", std::ios::binary | ios::app);
    if (!arquivo) {
        rf.read
        std::cerr << "Erro ao criar o arquivo." << std::endl;
        return 0;
    }
    arquivo.close();
    std::cout << "Arquivo criado com sucesso." << std::endl;
}

void incluirVendedor() {
    Vendedor novoVendedor;
    std::cout << "Digite o código do vendedor: ";
    std::cin >> novoVendedor.codigo;

    std::ifstream arquivoLeitura("VENDAS.DAT", std::ios::binary | ios::app);
    if (!arquivoLeitura) {
        rf.read
        std::cerr << "Erro ao abrir o arquivo." << std::endl;
        cout << endl;
        return 0;
    }

    while (arquivoLeitura.read(reinterpret_cast<char*>(&novoVendedor), sizeof(Vendedor))) {
        if (novoVendedor.codigo == novoVendedor.codigo && novoVendedor.mes == novoVendedor.mes) {
            std::cout << "Já existe um vendedor com o mesmo código e mês de vendas." << std::endl;
            cout << endl;
            arquivoLeitura.close();
            return 0;
        }
    }
    
    ArquivoLeitura.close();

    
    std::ofstream arquivoEscrita("VENDAS.DAT", std::ios::binary | std::ios::app);
    if (!arquivoEscrita) {
        std::cerr << "Erro ao abrir o arquivo." << std::endl;
        cout << endl; 
        return 0;

         }

    std::cout << "Digite o nome do vendedor: ";
    std::cin.ignore();
    std::cin.getline(novoVendedor.nome, 50);
    std::cout << "Digite o valor da venda: ";
    std::cin >> novoVendedor.valorVenda;
    std::cout << "Digite o mês da venda: ";
    std::cin >> novoVendedor.mes;

    arquivoEscrita.write(reinterpret_cast<const char*>(&novoVendedor), sizeof(Vendedor));
    arquivoEscrita.close();

    std::cout << "Vendedor incluído com sucesso." << std::endl;
}
