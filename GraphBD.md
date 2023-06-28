'''mermaid
graph BD
classDiagram
    class EmpresaParceira {
        + ID : string
        + Nome : string
        + Endereço : string
        + Contato : string
    }
    class Tecnologia {
        + ID : string
        + Nome : string
        + Área : string
    }
    class RegistroTecnologiasUtilizadas {
        + ID : string
        + ID_Empresa : string
        + ID_Tecnologia : string
    }
    class Colaborador {
        + ID : string
        + Nome : string
        + Cargo : string
        + ID_Empresa : string
    }
    
    EmpresaParceira "1" -- "n" Tecnologia : possui
    Tecnologia "1" -- "n" RegistroTecnologiasUtilizadas : presente em
    EmpresaParceira "1" -- "n" Colaborador : possui
