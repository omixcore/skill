# 科研绘图统一标准 / Scientific Figure Standards

## 中文版

绘图统一采用以下标准：

- **页面**：A4 竖版，四周页边距不超过 25 mm；合理布局，不必铺满整页。
- **字体**：Arial，7 pt，不加粗，颜色为纯黑色（`#000000`）。
- **线条**：纯黑色（`#000000`），线宽 0.5 pt。
- **箭头**：箭头与连接线为一体，避免分离或错位。
- **输出格式**：优先同时提供 **PDF 和 SVG** 矢量文件。
- **可编辑性**：文字、线条、箭头、图形等各个元素均可独立编辑；文字保留为文本，不转曲，整图不栅格化。
- **复制与缩放**：保持图形比例和元素相对位置，确保复制、粘贴及等比例缩放后不变形、不发生排版错位。
- **布局**：比例协调、对齐规范、间距适当，避免拥挤或过度留白。

## 参考图片风格、配色与布局 / Reference-driven Style, Color, and Layout

绘图时应优先参考用户提供的图片，以及仓库 `plotting/references/` 中归档的图片。开始绘图前，先查看参考图片并提炼其视觉规范，再应用到新图中。

- **整体风格**：模仿参考图的视觉语言，包括图形表现方式、线型、边框、标记形状、背景、坐标轴、图例、注释方式和文字层级。保持整体风格协调，不随意套用与参考图不一致的默认主题。
- **配色体系**：优先沿用参考图的主色、辅助色、强调色和背景色，匹配其色相关系、明度、饱和度及对比度。尽可能保持不同类别、组织、处理组或数据类型的颜色映射一致；必要时记录对应的 HEX/RGB 色值，供后续图件复用。不得无故改成花哨或高饱和度配色；若可读性或色盲友好性不足，应在不破坏整体风格的前提下做最小调整。
- **排版布局**：参考原图的分面顺序、行列结构、模块比例、图文比例、对齐方式、模块间距、留白、标题与图例位置及视觉层级。按本次数据量和科学叙事合理适配，不为填满页面而拉伸图形或改变比例。
- **模仿边界**：只借鉴风格、配色和布局，不照搬参考图中的数据、结论、实验内容或不适用于当前研究的标注。所有数值、统计结果、图例和生物学解释必须来自本次真实数据并经过核对。
- **与统一标准的关系**：参考图的风格要求与本文件中的页面、字体、线宽、可编辑性等硬性规范同时执行；如有冲突，默认保留统一标准，只有用户明确要求时才调整。
- **参考图归档**：用户提供的原始参考图片也必须作为实际图片文件提交到仓库，统一存放在 `plotting/references/`，不能只在文字中描述或仅保留网页预览。尽量保留原始文件，不压缩、不重绘、不覆盖；文件名应清晰稳定，并在该目录的 README 中登记图片名称、来源（已知时）、主要配色和布局特征。
- **缺少图片时**：如果本次任务提到的参考图片在当前可访问文件中不可用，应请用户重新上传，不得凭印象猜测具体颜色、布局或图形细节。

## English Version

Apply the following standards to all figures:

- **Page setup**: Use A4 portrait orientation with margins of no more than 25 mm on all sides. Arrange the content appropriately; it does not need to fill the entire page.
- **Typography**: Use Arial, 7 pt, regular weight (not bold), with all text in pure black (`#000000`).
- **Lines**: Use pure black (`#000000`) with a line width of 0.5 pt.
- **Arrows**: Keep each arrowhead and its connecting line integrated as a single object to prevent separation or misalignment.
- **Output formats**: Preferably provide both **PDF and SVG** vector files.
- **Editability**: All elements, including text, lines, arrows, and shapes, must be independently editable. Preserve text as text rather than converting it to outlines, and do not rasterize the entire figure.
- **Copying and scaling**: Preserve aspect ratios and the relative positions of all elements. Copying, pasting, and proportional scaling must not introduce distortion or layout shifts.
- **Layout**: Maintain balanced proportions, consistent alignment, and appropriate spacing. Avoid overcrowding and excessive empty space.

## Reference-driven Style, Color, and Layout

Use user-supplied figures and the images archived in `plotting/references/` as visual references. Before creating a new figure, inspect the available references and extract their visual conventions.

- **Overall style**: Follow the reference figures' visual language, including graphic treatment, line styles, borders, marker shapes, backgrounds, axes, legends, annotation methods, and typographic hierarchy. Avoid applying an unrelated default theme.
- **Color palette**: Prefer the reference figures' primary, secondary, accent, and background colors. Match their hue relationships, lightness, saturation, and contrast. Keep color mappings consistent across categories, tissues, treatment groups, and data types; record HEX/RGB values when useful for reuse. Do not introduce flashy or unnecessarily saturated colors. If readability or color accessibility is insufficient, make the smallest adjustments that preserve the overall visual style.
- **Composition and layout**: Follow the reference figures' panel order, row/column structure, relative panel sizes, text-to-graphic proportions, alignment, spacing, whitespace, title and legend placement, and visual hierarchy. Adapt the composition to the current data and scientific narrative without stretching elements or changing their proportions merely to fill the page.
- **Imitation boundaries**: Borrow only the visual style, palette, and layout. Do not copy the reference figures' data, conclusions, experimental content, or annotations that do not apply to the current study. All values, statistics, legends, and biological interpretations must come from the current data and be checked for accuracy.
- **Relationship to the core standards**: Apply these reference-driven preferences together with the page, typography, line-width, and editability requirements in this document. If they conflict, retain the core standards unless the user explicitly requests an exception.
- **Reference image archiving**: Commit the actual original reference image files to the repository under `plotting/references/`. Do not rely only on text descriptions or web previews. Preserve original files whenever possible; do not compress, redraw, or overwrite them. Use clear, stable filenames and register each image in that directory's README with its filename, source (if known), and key palette and layout characteristics.
- **Unavailable references**: If a referenced image is not accessible in the current task, ask the user to upload it again. Never guess its exact colors, layout, or graphic details from memory.
