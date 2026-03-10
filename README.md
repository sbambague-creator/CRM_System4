package src.crm.modelo;

import java.util.List;

public class GenerarReporte {
    private int numeroOportunidades;
    private double montoTotal;
    
    // Constructor
    public GenerarReporte() {
        this.numeroOportunidades = 0;
        this.montoTotal = 0.0;
    }
    
    // Getter y Setter
    public int getNumeroOportunidades() {
        return numeroOportunidades;
    }
    
    public void setNumeroOportunidades(int numeroOportunidades) {
        this.numeroOportunidades = numeroOportunidades;
    }
    
    public double getMontoTotal() {
        return montoTotal;
    }
    
    public void setMontoTotal(double montoTotal) {
        this.montoTotal = montoTotal;
    }
    
    // Método generarReporte
    public void generarReporte(List<Oportunidad> oportunidades) {
        System.out.println("=== GENERANDO REPORTE ===");
        
        this.numeroOportunidades = oportunidades.size();
        this.montoTotal = 0.0;
        
        for (Oportunidad opp : oportunidades) {
            this.montoTotal += opp.getMontoEstimado();
        }
        
        System.out.println("Número total de oportunidades: " + numeroOportunidades);
        System.out.println("Monto total estimado: $" + montoTotal);
        System.out.println("Monto promedio por oportunidad: $" + 
                          (numeroOportunidades > 0 ? montoTotal / numeroOportunidades : 0));
        System.out.println("=========================");
    }

}
