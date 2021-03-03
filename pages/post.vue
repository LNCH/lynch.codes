<template>
    <div class="container">
        <div>
            <header class="mega-header">
                <h1 class="article-title text-4xl">
                    How to Animate the Details Element
                </h1>
            </header>

            <div class="article-content">
                <p>Here’s a <a href="https://codepen.io/MoritzGiessmann/pen/PobErJB">nice simple demo</a>
                    from Moritz Gießmann on animating the triangle of a <code>&lt;details&gt;</code> element,
                    which is the <a
                        href="https://www.interaction-design.org/literature/topics/affordances">affordance</a> that
                    tells people <em>this thing can be opened</em>. Animating it, then is another kind of affordance
                    that tells people <em>this thing is opening now</em>. </p>
                <p>The tricks?</p>
                <ol>
                    <li>Turn off the default triangle: <code>details summary::-webkit-details-marker { display:none;
                        }</code>.
                        You can’t animate that one.
                    </li>
                    <li>Make a replacement triangle with <a href="https://css-tricks.com/snippets/css/css-triangle/">the
                        CSS border trick</a> and <a href="https://css-tricks.com/almanac/selectors/a/after-and-before/">a
                        pseudo element</a>.
                    </li>
                    <li>Animate the new triangle when the state is open: <code>details[open] &gt; summary::before {
                        transform: rotate(90deg); }</code>.
                    </li>
                </ol>


                <p>The <code>mask-type</code> CSS property indicates whether the SVG <code>&lt;mask&gt;</code> element
                    is treated as an alpha mask or a luminance mask.</p>
                <pre rel="CSS" class="wp-block-csstricks-code-block  language-css" data-line=""><code markup="tt"
                                                                                                      class=" language-css"><span
                    class="token selector">mask</span> <span class="token punctuation">{</span>
  <span class="token property">mask-type</span><span class="token punctuation">:</span> alpha<span
                        class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
                <p>When the mask layer is an image or a gradient, a <a
                    href="https://css-tricks.com/almanac/properties/m/mask-mode/"><code>mask-mode</code></a> property
                    can be set on the HTML element to specify the type of masking. However, if an SVG
                    <code>&lt;mask&gt;</code> element is used as the mask layer, the <code>mask-type</code> can be set
                    on the <code>&lt;mask&gt;</code> element itself. The <code>mask-mode</code> property can override
                    this preference.</p>
                <h3 id="h-syntax"><a href="#syntax" aria-hidden="true" class="aal_anchor" id="syntax">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Syntax
                </h3>
                <pre rel="CSS" class="wp-block-csstricks-code-block  language-css" data-line=""><code markup="tt"
                                                                                                      class=" language-css"><span
                    class="token property">mask-type</span><span
                    class="token punctuation">:</span> alpha | luminance</code></pre>
                <p>The property accepts one keyword value of the alpha and luminance values.</p>
                <ul class="ticss-f33ad05a">
                    <li><strong>Initial value:</strong> <code>luminance</code></li>
                    <li><strong>Applies to:</strong> <code>&lt;mask&gt;</code> elements</li>
                    <li><strong>Inherited:</strong> no</li>
                    <li><strong>Computed value:</strong> absolute length</li>
                    <li><strong>Animation type:</strong> discrete</li>
                </ul>
                <h3 id="h-values"><a href="#values" aria-hidden="true" class="aal_anchor" id="values">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Values
                </h3>
                <pre rel="CSS" class="wp-block-csstricks-code-block  language-css" data-line=""><code markup="tt"
                                                                                                      class=" language-css"><span
                    class="token comment">/* Keyword values */</span>
<span class="token property">mask-type</span><span class="token punctuation">:</span> alpha<span
                        class="token punctuation">;</span>
<span class="token property">mask-type</span><span class="token punctuation">:</span> luminance<span
                        class="token punctuation">;</span>

<span class="token comment">/* Global values */</span>
<span class="token property">mask-type</span><span class="token punctuation">:</span> inherit<span
                        class="token punctuation">;</span>
<span class="token property">mask-type</span><span class="token punctuation">:</span> initial<span
                        class="token punctuation">;</span>
<span class="token property">mask-type</span><span class="token punctuation">:</span> unset<span
                        class="token punctuation">;</span></code></pre>
                <ul>
                    <li><code>luminance</code>: The default value. The luminance values of the mask are used for the
                        mask values.
                    </li>
                    <li><code>alpha</code>: The alpha values (alpha channel) of the mask are used for the mask values.
                    </li>
                    <li><code>initial</code>: Applies the property’s default value, <code>luminance</code>.</li>
                    <li><code>inherit</code>: Adopts the <code>mask-type</code> value of the parent.</li>
                    <li><code>unset</code>: Removes the current <code>mask-type</code> from the element.</li>
                </ul>
                <h3 id="h-alpha-and-luminance-masks"><a href="#alpha-and-luminance-masks" aria-hidden="true"
                                                        class="aal_anchor" id="alpha-and-luminance-masks">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Alpha and luminance masks
                </h3>
                <p>Alpha? Luminance? It’s worth visiting these terms as they relate to CSS masking.</p>
                <h4 id="h-alpha-masks"><a href="#alpha-masks" aria-hidden="true" class="aal_anchor" id="alpha-masks">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Alpha masks
                </h4>
                <p>Images are made of pixels, where each pixel contains color values. And some color values contain an
                    <strong>alpha channel</strong> to set transparency on the color. An image with an alpha channel can
                    be an <strong>alpha mask</strong>, like PNG images with transparent areas.</p>
                <p>In a simple masking operation, we have an element and a mask image placed on top of it. The alpha
                    value of each pixel in the mask image will be merged with its corresponding pixel in the
                    element.</p>
                <ul>
                    <li>If the alpha value is zero (i.e. transparent), it wins out and that part of the element is
                        masked (i.e. hidden).
                    </li>
                    <li>An alpha value of one (i.e. fully opaque) displays those pixels.</li>
                    <li>An alpha value between 0 and 1 (e.g. 0.5) allows the pixel to be visible, but with a certain
                        level of transparency.
                    </li>
                </ul>
                <p>Bottom line, the mask value at a given point is the value of the alpha channel at that point of the
                    mask image. If that point is fully transparent (i.e. alpha value of 0), then it won’t display. The
                    reverse is true with a fully opaque (i.e. alpha value of 1), where that point is fully
                    displayed.</p>
                <p>The example bellow is an alpha mask that only contains black (i.e. alpha value of 1) and transparent
                    areas (i.e. alpha value of 0).</p>
                <figure class="wp-block-image size-full"><img loading="lazy" width="1000" height="700"
                                                              src="https://i2.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418224888_alpha-mask-1.jpg?resize=1000%2C700&amp;ssl=1"
                                                              alt="" class="wp-image-335416"
                                                              srcset="https://i2.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418224888_alpha-mask-1.jpg?w=1000&amp;ssl=1 1000w, https://i2.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418224888_alpha-mask-1.jpg?resize=300%2C210&amp;ssl=1 300w, https://i2.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418224888_alpha-mask-1.jpg?resize=768%2C538&amp;ssl=1 768w"
                                                              sizes="(min-width: 735px) 864px, 96vw"
                                                              data-recalc-dims="1"></figure>
                <h4 id="h-luminance-masks"><a href="#luminance-masks" aria-hidden="true" class="aal_anchor"
                                              id="luminance-masks">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Luminance masks
                </h4>
                <p>In a <strong>luminance mask</strong>, colors and alpha values matter. When the alpha value is 0 (i.e.
                    fully transparent), the element is hidden. The mask values vary depending on the color channel of
                    that pixel when the alpha value is 1. For example, when the color is white, the element is visible;
                    in the case of black area, the element is hidden.</p>
                <p>We saw that calculating mask values in an <strong>alpha mask</strong> is based only on the alpha
                    values of the mask image. On the flip side, the mask values of a <strong>luminance mask</strong> are
                    computed from <em>both</em> the luminance and alpha values. Here’s how the browser responds:</p>
                <ol>
                    <li>First, it computes a luminance value from the color channel values.</li>
                    <li>Then, it multiplies that computed luminance value by the corresponding alpha value to produce
                        the mask value.
                    </li>
                </ol>
                <p class="explanation">Check out the <a href="https://drafts.fxtf.org/css-masking-1/#MaskValues">CSS
                    Masking Module 1 specification</a> from the September 2019 Editor’s Draft for more information.</p>
                <p>Below is the same exact example we saw for alpha masks, but with a difference: This time, we have a
                    fully opaque white area in the center (instead of black) surrounded by transparent areas around it.
                    As you can see, the white area is fully visible just as it was with the black alpha mask:</p>
                <figure class="wp-block-image size-full"><img loading="lazy" width="1000" height="700"
                                                              src="https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418435637_luminance-mask-1.jpg?resize=1000%2C700&amp;ssl=1"
                                                              alt="" class="wp-image-335417"
                                                              srcset="https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418435637_luminance-mask-1.jpg?w=1000&amp;ssl=1 1000w, https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418435637_luminance-mask-1.jpg?resize=300%2C210&amp;ssl=1 300w, https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/02/s_ADCFB9F0494AC50BE88B2195592C05580BDEAAC4ECC0BBBFE6BE461D40F61FF7_1611418435637_luminance-mask-1.jpg?resize=768%2C538&amp;ssl=1 768w"
                                                              sizes="(min-width: 735px) 864px, 96vw"
                                                              data-recalc-dims="1"></figure>
                <h3 id="h-example"><a href="#example" aria-hidden="true" class="aal_anchor" id="example">
                    <svg aria-hidden="true" class="aal_svg" height="16" version="1.1" viewBox="0 0 16 16" width="16">
                        <path fill-rule="evenodd"
                              d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path>
                    </svg>
                </a>Example
                </h3>
                <p>The following example is using a mask element with black and transparent areas:</p>
                <pre rel="HTML" class="wp-block-csstricks-code-block  language-html" data-line=""><code markup="tt"
                                                                                                        class=" language-html"><span
                    class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>div</span><span
                    class="token punctuation">&gt;</span></span>Put a nice mask on me!<span class="token tag"><span
                    class="token tag"><span class="token punctuation">&lt;/</span>div</span><span
                    class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>svg</span><span
    class="token punctuation">&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>mask</span> <span
      class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation">=</span><span
      class="token punctuation">"</span>mask<span class="token punctuation">"</span></span><span
      class="token punctuation">&gt;</span></span>
    <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>path</span> <span
        class="token attr-name">fill</span><span class="token attr-value"><span class="token punctuation">=</span><span
        class="token punctuation">"</span>black<span class="token punctuation">"</span></span> <span
        class="token attr-name">d</span><span class="token attr-value"><span class="token punctuation">=</span><span
        class="token punctuation">"</span>M10,35 A20,20,0,0,1,50,35 A20,20,0,0,1,90,35 Q90,65,50,95 Q10,65,10,35 Z<span
        class="token punctuation">"</span></span> <span class="token punctuation">/&gt;</span></span>
  <span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>mask</span><span
      class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>svg</span><span
    class="token punctuation">&gt;</span></span></code></pre>
                <p>Using the element’s ID (<code>#mask</code>), we can place the mask on the <code>&lt;div&gt;</code>
                    element.</p>
                <pre rel="HTML" class="wp-block-csstricks-code-block  language-html" data-line="5"><code markup="tt"
                                                                                                         class=" language-html">div {
  width: 100px;
  height: 100px;
  background-color: #134;
  mask-image: url(#mask);
}    <div aria-hidden="true" data-range="5" class=" line-highlight" data-start="5" style="top: 112px;">
</div></code></pre>
                <p>Since this mask has black and transparent areas, we set <code>mask-type</code> to <code>alpha</code>:
                </p>
                <pre rel="CSS" class="wp-block-csstricks-code-block  language-css" data-line=""><code markup="tt"
                                                                                                      class=" language-css"><span
                    class="token selector">mask</span> <span class="token punctuation">{</span>
  <span class="token property">mask-type</span><span class="token punctuation">:</span> alpha<span
                        class="token punctuation">;</span>
<span class="token punctuation">}</span></code></pre>
                <p>If the path element had white areas, the default value, <code>luminance</code>, would work perfectly
                    fine here instead.</p>

                <h3 id="h-browser-support">Browser support</h3>

                <figure class="wp-block-table ticss-2969c85c">
                    <table class="has-fixed-layout">
                        <thead>
                        <tr>
                            <th class="has-text-align-center" data-align="center">IE</th>
                            <th class="has-text-align-center" data-align="center">Edge</th>
                            <th class="has-text-align-center" data-align="center">Firefox</th>
                            <th class="has-text-align-center" data-align="center">Chrome</th>
                            <th class="has-text-align-center" data-align="center">Safari</th>
                            <th class="has-text-align-center" data-align="center">Opera</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td class="has-text-align-center" data-align="center">No</td>
                            <td class="has-text-align-center" data-align="center">79+</td>
                            <td class="has-text-align-center" data-align="center">35+</td>
                            <td class="has-text-align-center" data-align="center">24+</td>
                            <td class="has-text-align-center" data-align="center">6.1+</td>
                            <td class="has-text-align-center" data-align="center">15+</td>
                        </tr>
                        </tbody>
                    </table>
                </figure>

                <figure class="wp-block-table ticss-1679a4e0">
                    <table class="has-fixed-layout">
                        <thead>
                        <tr>
                            <th class="has-text-align-center" data-align="center">Android Chrome</th>
                            <th class="has-text-align-center" data-align="center">Android Firefox</th>
                            <th class="has-text-align-center" data-align="center">Android Browser</th>
                            <th class="has-text-align-center" data-align="center">iOS Safari</th>
                            <th class="has-text-align-center" data-align="center">Opera Mobile</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td class="has-text-align-center" data-align="center">Yes</td>
                            <td class="has-text-align-center" data-align="center">Yes</td>
                            <td class="has-text-align-center" data-align="center">81+</td>
                            <td class="has-text-align-center" data-align="center">7+</td>
                            <td class="has-text-align-center" data-align="center">59+</td>
                        </tr>
                        </tbody>
                    </table>
                    <figcaption>
                        Source: <a href="https://caniuse.com/mdn-css_properties_mask-type">caniuse</a>
                    </figcaption>
                </figure>

            </div>

        </div>
    </div>
</template>