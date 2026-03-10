package src.crm.principal;
import java.time.LocalDateTime;
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;  // ← Importar Scanner

import src.crm.modelo.Cliente;
import src.crm.modelo.GenerarReporte;
import src.crm.modelo.Oportunidad;

public class Main {
    public static void main(String[] args){
        
        // Crear clientes
        Cliente cliente1 = new Cliente(1, "Empresa ABC", "123456789", 
                                      "contacto@empresaabc.com", LocalDateTime.now());
        Cliente cliente2 = new Cliente(2, "Corporación XYZ", "987654321", 
                                      "info@corporacionxyz.com", LocalDateTime.now());
        
        // Almacenar clientes en una lista para poder buscarlos
        List<Cliente> clientes = new ArrayList<>();
        clientes.add(cliente1);
        clientes.add(cliente2);
        
        // Consultar clientes inicialmente
        cliente1.consultarCliente();
        cliente2.consultarCliente();
        
        // Crear oportunidades
        Oportunidad opp1 = new Oportunidad(1, 50000.0, LocalDateTime.now(), "Pendiente");
        Oportunidad opp2 = new Oportunidad(2, 75000.0, LocalDateTime.now(), "Pendiente");
        Oportunidad opp3 = new Oportunidad(3, 120000.0, LocalDateTime.now(), "En Proceso");
        
        // Asignar oportunidades a clientes
        opp1.setCliente(cliente1);
        opp2.setCliente(cliente1);
        opp3.setCliente(cliente2);
        
        // Mostrar oportunidades
        opp1.mostrarOportunidad();
        opp2.mostrarOportunidad();
        opp3.mostrarOportunidad();
        
        // Cambiar estado de una oportunidad
        opp1.cambiarEstado();
        
        // Generar reporte
        List<Oportunidad> oportunidades = new ArrayList<>();
        oportunidades.add(opp1);
        oportunidades.add(opp2);
        oportunidades.add(opp3);
        
        GenerarReporte reporte = new GenerarReporte();
        reporte.generarReporte(oportunidades); 
        }
}
