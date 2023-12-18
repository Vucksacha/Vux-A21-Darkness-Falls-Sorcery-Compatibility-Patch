# Alpha 21 Darkness Falls & Sorcery Compatibility patch

Make sure you read this - the HUD won't load properly if you don't manually do the step at the bottom.

Darkness Falls 5.0.1 and Sorcery 1.942

Credit to Sorcerer NotARobot for the previous compatibility patches, quite a lot of what NotARobot developed is still very relevant and is incorporated in to the changes here.

Have to change the following in 0-DarknessFallsCore/Config/XUi/xui.xml:
From:
	<set xpath="/xui/ruleset/window_group[@name='toolbelt']">
		<window name="DFToolbelt" anchor="CenterBottom" />
		<window name="DFXpBar" anchor="CenterBottom" />
		<window name="DFToolbeltTexture" anchor="CenterBottom" />
		<window name="HUDBuffPopout" anchor="LeftBottom" />
		<window name="HUDLeftStatBars" anchor="CenterBottom" />
		<window name="HUDRightStatBars" anchor="RightBottom" />
		<window name="windowQuestTracker" anchor="RightTop" />
		<window name="windowGroupBars" anchor="LeftTop" />	
	</set>

To:
	<append xpath="/xui/ruleset/window_group[@name='toolbelt']">
		<window name="HUDBuffPopout" anchor="LeftBottom" />
		<window name="HUDLeftStatBars" anchor="CenterBottom" />
	</append>