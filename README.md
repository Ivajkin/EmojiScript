# EmojiScript Cloud Hub AI

Example showcase:
```typescript
import * as React from "react";
import { useState } from "react";
import { Button } from "@blueprintjs/core";
import { getNewModalInstance } from "src/components/modals/genericModal/GenericModalView";
import { ModifyUnitTypeView } from "src/components/domains/unitConversion/modals/unitType/modifyUnitTypeModal/ModifyUnitTypeView";
import { localeUtils } from "src/testUtils/locale";
import { unitConversionApi } from "src/generated-code/api/unitConversionApi";
import UnitType = unitConversionApi.models.UnitType;

/**
 * Displays unit type. Mock to be deleted after merge of ... changes.
 * @param unitType is unit type to display.
 * @param updateOnChange is callback to refresh when unit type is changed.
 * @constructor
 */
export const UnitTypeMock = ({
    unitType,
    updateOnChange
}: {
    /**
     * Unit type to display.
     */
    unitType: UnitType;
    /**
     * Callback to refresh when unit type is changed.
     * @param unitType is unit type to update.
     */
    updateOnChange: (unitType: UnitType) => void;
}) => {
    const [generatedUUID, setGeneratedUUID] = useState("");

    return (
        <div>
            {JSON.stringify(unitType)}

            <div>
                <Button
                    text={"Change"}
                    onClick={() => {
                        setGeneratedUUID(getNewModalInstance());
                    }}
                />
                <ModifyUnitTypeView
                    onSave={(name: string) => {
                        updateOnChange({ ...unitType, name: name });
                    }}
                    localeUtils={localeUtils}
                    isUnitTest={false}
                    currentModalInstanceId={generatedUUID}
                    unitType={unitType}
                />
            </div>
        </div>
    );
};
```

becomes

```typescript
⇢ * as ⚡️ ⇠ 🌩
➡️🚢⬅️🌩
➡️ℹ️⬅️"@blueprintjs/core";
➡️🌊🆕🪟1️⃣⬅️"🫀/⚙️s/📳s/generic🪟/Generic🪟🌁";
➡️🔄𝍥ឱ🌁⬅️"🫀/⚙️s/⩤s/𝍥💱/📳s/𝍥ឱ/🖋𝍥ឱ🪟/🔄𝍥ឱ🌁";
➡️👅📎s⬅️"🫀/🧪📎s/👅";
➡️𝍥💱📡⬅️"🫀/💥-🔐/🗜/𝍥💱📡";
⇢ 𝍥ឱ = 𝍥💱📡.👩🏻‍🦳s.𝍥ឱ;

/**
 * D⋕plays 𝍥 type. ☕️ to be deleted after merge of ᠅ changes.
 * @param 𝍥ឱ ⋕ 𝍥 type to 👀.
 * @param 🆕🔛🐒 ⋕ callback to refresh when 𝍥 type ⋕ changed.
 * @constructor
 */
export const 𝍥ឱ☕️ = ({
                                 𝍥ឱ,
                                 🆕🔛🐒
                             }: {
    /**
     * 𝍥 type to 👀.
     */
    𝍥ឱ: 𝍥ឱ;
    /**
     * Callback to refresh when 𝍥 type ⋕ changed.
     * @param 𝍥ឱ ⋕ 𝍥 type to 🆕.
     */
    🆕🔛🐒: (𝍥ឱ: 𝍥ឱ) => void;
}) => {
    const [💥🏷, 🪑Generated🏷] = 🚢(""🔚

    ⮑
        🔳
            {⤳(𝍥ឱ)}

            🔳
                <ℹ️
                    📕🐒"}
                    ʘ) => {
                        🪑Generated🏷(🌊🆕🪟1️⃣()🔚
                    }}
                />
                <🔄𝍥ឱ🌁
                    🦌📇: 🪢) => {
                        🆕🔛🐒({ ᠅𝍥ឱ, 📇: 📇 }🔚
                    }}
                    👅📎s={👅📎s}
                    ⋕𝍥🧪={false}
                    current🪟1️⃣Id={💥🏷}
                    𝍥ឱ={𝍥ឱ}
                />
            ⬜️
        ⬜️
    🔚
🔚
```



## Repo Structure


## How to Set Up


## How to Run in Development


## How to Test


## How to Build


## How to Run in Production


## Miscellaneous


## Additional Resources

