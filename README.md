# Exercicio-Java
package Roberta.Com.Agenda;

import org.jetbrains.annotations.NotNull;

import java.io.BufferedWriter;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class Persistente {
    private static final String arquivo = "contatos.txt";

    public static void criarArquivo(){
    try

    {
        File file = new File(arquivo);
        if (file.createNewFile()) {
            System.out.println("arquivo criado com sucesso");
        }
    }catch(IOException EX){
       System.out.println("erro de arquivo");
    }
    }
    public static void inserir(Java.@NotNull contato contato) {
        FileWriter FileWriter = null;
        try {
            FileWriter = new FileWriter(Persistente.arquivo, true);
            BufferedWriter buffer = new BufferedWriter(FileWriter);
            buffer.write((contato.getNome()+ ";")+ contato.getTelefone()+ contato.getEmail());
        } catch (IOException e) {
            throw new RuntimeException(e);
        }

    }
    }

