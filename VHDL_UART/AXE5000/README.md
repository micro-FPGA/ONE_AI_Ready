AXE5000 has on-board 25MHz oscillator, so you have two choices, use 25MHz as is and modify the clock and baudrate constants or adding a PLL that generates 100MHz.

    // Use 100MHz clock as main system clock
    //assign system_clk = hvio_pllrefclk;
    
	 
    PLL25M100 PLL(
        .refclk(hvio_pllrefclk ),
        .rst(1'b0 ),
        .outclk_0(system_clk ),
        .locked( ));	 


