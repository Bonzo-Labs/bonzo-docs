# Supply Rate Methodology

Borrow interest rates paid are distributed as yield for aToken holders who have supplied assets in the protocol, excluding a share of yields sent to the ecosystem reserve defined by the reserve factor on a per asset basis.

The deposit interest rate is paid on assets supplied, which is shared amongst all liquidity providers. The deposit APY $$D_t$$ is:

$$
D_t = U_t(VB_tV_t)(1 - R_t)
$$

* $$U_t$$ = the utilization ratio
* $$VB_t$$ = the share of variable borrows
* $$V_t$$ = the variable rate
* $$R_t$$ = the reserve factor
