module down_counter_4bit (
    input clk,
    input reset,
    output reg [3:0] count
);
always @(posedge clk or posedge reset) begin
    if (reset)
    begin
        count <= 4'b1111;
    end
    else begin
        count <= count - 1'b1;
     end
end
endmodule
