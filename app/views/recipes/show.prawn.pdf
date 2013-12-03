prawn_document() do |pdf|
  pdf.text @recipe.name
  pdf.move_down 100
  pdf.stroke_horizontal_rule
  pdf.move_down 5
  pdf.image URI.parse(@recipe.image).open, width: 400, position: :center
  pdf.move_down 5
  pdf.stroke_horizontal_rule

  pdf.table([
    ["Course", @recipe.course],
    ["Cooktime", @recipe.cooktime],
    ["Serving size", @recipe.servingsize]
  ], width: 300)
  
  pdf.text @recipe.instructions

  @recipe.ingredients.each do |ingredient|
    pdf.text ingredient.name
    pdf.move_down 10
    pdf.image URI.parse(ingredient.image).open, width: 100
    pdf.stroke_horizontal_rule
  end

  pdf.start_new_page

  pdf.rotate(-30, origin: [250, 200]) do 
    pdf.image URI.parse(@recipe.image).open, width: 200
  end

  pdf.span(350, position: :center) do
    pdf.text "Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit. Lorem	ipsum dolor sit amet, consectetur adipiscing elit."
  end
end