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
â¢ * as â¡ï¸ â  ð©
â¡ï¸ð¢â¬ï¸ð©
â¡ï¸â¹ï¸â¬ï¸"@blueprintjs/core";
â¡ï¸ðððª1ï¸â£â¬ï¸"ð«/âï¸s/ð³s/genericðª/Genericðªð";
â¡ï¸ðð¥á±ðâ¬ï¸"ð«/âï¸s/â©¤s/ð¥ð±/ð³s/ð¥á±/ðð¥á±ðª/ðð¥á±ð";
â¡ï¸ððsâ¬ï¸"ð«/ð§ªðs/ð";
â¡ï¸ð¥ð±ð¡â¬ï¸"ð«/ð¥-ð/ð/ð¥ð±ð¡";
â¢ ð¥á± = ð¥ð±ð¡.ð©ð»âð¦³s.ð¥á±;

/**
 * Dâplays ð¥ type. âï¸ to be deleted after merge of á  changes.
 * @param ð¥á± â ð¥ type to ð.
 * @param ððð â callback to refresh when ð¥ type â changed.
 * @constructor
 */
export const ð¥á±âï¸ = ({
                                 ð¥á±,
                                 ððð
                             }: {
    /**
     * ð¥ type to ð.
     */
    ð¥á±: ð¥á±;
    /**
     * Callback to refresh when ð¥ type â changed.
     * @param ð¥á± â ð¥ type to ð.
     */
    ððð: (ð¥á±: ð¥á±) => void;
}) => {
    const [ð¥ð·, ðªGeneratedð·] = ð¢(""ð

    â®
        ð³
            {â¤³(ð¥á±)}

            ð³
                <â¹ï¸
                    ðð"}
                    Ê) => {
                        ðªGeneratedð·(ðððª1ï¸â£()ð
                    }}
                />
                <ðð¥á±ð
                    ð¦ð: ðª¢) => {
                        ððð({ á ð¥á±, ð: ð }ð
                    }}
                    ððs={ððs}
                    âð¥ð§ª={false}
                    currentðª1ï¸â£Id={ð¥ð·}
                    ð¥á±={ð¥á±}
                />
            â¬ï¸
        â¬ï¸
    ð
ð
```



## Repo Structure


## How to Set Up


## How to Run in Development


## How to Test


## How to Build


## How to Run in Production


## Miscellaneous


## Additional Resources

