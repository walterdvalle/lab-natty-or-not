# Conversão de código java em Mermaid Syntax

## 📒 Descrição
Automatizar a fase de projetos de sistemas de informação usando geração automatizada de diagramas.

## 🤖 Tecnologias Utilizadas
ChaTGPT E código Java

## 🧐 Processo de Criação
Um conjunto de classes Java que representam uma parte do domínio de um sistema foram inseridos no ChatGPT e o resultado foi adicionado abaixo.

## 🚀 Resultados
Um diagrama de classes em Mermaid Syntax.

classDiagram
    class AeroportoDTO {
        BigInteger id
        String nome
        String iata
        MunicipioDTO municipio
        ConcessionariaDTO concessionaria
    }
    
    class ConcessionariaDTO {
        BigInteger id
        String nome
        String cnpj
    }

    class EstadoDTO {
        BigInteger id
        String sigla
        String nome
        PaisDTO pais
    }

    class MunicipioDTO {
        BigInteger id
        String nome
        EstadoDTO estado
        boolean capital
    }

    class PaisDTO {
        BigInteger id
        String nome
        String siglaISO
        String codigoONU
        String nomeIngles
    }

    AeroportoDTO --> MunicipioDTO
    AeroportoDTO --> ConcessionariaDTO
    MunicipioDTO --> EstadoDTO
    EstadoDTO --> PaisDTO
