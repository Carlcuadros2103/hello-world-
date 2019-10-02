llama
@startuml

class person{
    String name
    Int DNI
}
class client{
    String user
    String pasword
    void register()
    void consult()
    void reserve_movie()
}
class admin{
    String pasword
    void modify_client()
    void delete_client()
}
class reservation{
    client tipeclient
    movie tipemovie
    card tipecard
    void consulte_reserve()
    void consulte_buy()
}
class movie{
    String director
    String genero
    String languaje
    String sinopsis
    double duration
    double coste_rent
    double coste_buy
    void verify_info()
    void save_movie()
    void buy()
    void rent()
}
class card{
    int id_card
    int punts
    double salde
}

person <|-- client
person <|-- admin
reservation *-- card
reservation *-- movie
reservation *-- client



@enduml
