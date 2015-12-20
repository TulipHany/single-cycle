# single-cycle
module PC (Clk, In1, In2, Slin2, Branch, Alu0,sum,PcSrc, Pci, Pco);
//}} End of automatically maintained section

input  wire In1, In2, Slin2,Branch, Alu0, Pci, Clk; 
output reg sum,PcSrc;
output reg Pco;
// -- Enter your statements here -- //
SLT (Slin2, In2, 2);
AND (PcSrc, Branch, Alu0);
ADD (Sum, Slin2, In1);
begin
always @ (posedge Clk)
	assign Pco = Pci;
end
endmodule
