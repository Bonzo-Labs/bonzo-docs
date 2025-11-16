# Enable / Disable Collateral

Enabling and disabling supplied assets as collateral allows for more nuanced control over one's lending and borrowing strategy within the protocol.

Assets supplied to Bonzo Finance are enabled as collateral by default. This means that after an asset is supplied to the protocol, users can then borrow against a percentage of the total value supplied. This percentage is called the "loan-to-value ratio (LTV)" and varies for each asset based on its individual risk profile.

It's important to note that assets supplied as collateral are only susceptible to liquidation if the user is borrowing other assets against its value. If you're not borrowing, your supplied assets cannot be liquidated, even if they are enabled as collateral. In addition, reward APYs continue to accrue when supplying an asset, even if it's disabled as collateral.

Bonzo Finance allows users to "enable" or "disable" whether an asset supplied is used as collateral or not. There are a few reasons why a user might want to utilize this feature on a per-asset basis:

1. **Risk management**: By disabling an asset as collateral, you prevent it from being used to borrow against, which can help manage your overall risk exposure.
2. **Avoiding liquidation risk**: If you don't want a particular asset to be at risk of liquidation, you can disable it as collateral.
3. **Strategic borrowing**: You may want to use only specific assets as collateral based on your borrowing strategy or market conditions.
4. **Simplifying position management**: By limiting which assets are used as collateral, you can make it easier to track and manage your positions.
5. **Yield optimization**: Some users may prefer to keep certain high-yielding assets separate from their collateral pool to maximize returns without increasing borrowing capacity.

### Enabling & Disabling Assets as Collateral:

1. View the "Supplied" box in the Bonzo Finance interface.
2. Find the asset you'd like to enable or disable as collateral and click on its <img src="../../.gitbook/assets/image (4).png" alt="" data-size="line"> button in the table.
3. Click "Disable as Collateral" or "Enable as Collateral" from the drop-down menu.
4. An on-screen modal will appear confirming details of this transaction — once reviewed, click the "Disable as Collateral" or "Enable as Collateral" button.
5. Review the transaction in your connected wallet and approve.
