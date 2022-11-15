# Soft returns cause viewing and diff problems

A soft return is a single line return in the middle of a paragraph block. In Markdown such are handled the same as an extra space and ignored. However, this practice has always been controversial.

For instance, lines that have the exact same words on them will be reported by `diff` and other tools just for reformatting.

Content creators can also never agree on what the optimal column width should be: 80, 72, 108? This creates huge frustration because one wrap column width looks great for someone while another one looks horrible.

Better to let the content creator and consume decide *their* preferred column width so that they can view it on the most things without a problem. This is in line with Gruber's "source should be as readable as the render" principle. Whether a reader has minimized a TMUX pane to 10x10 in a corner or filled the screen, the automatic wrapping will remain as readable as possible.
