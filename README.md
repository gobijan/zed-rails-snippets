# Ruby on Rails Snippets for Zed Editor

This repository contains a collection of snippets for the Zed Editor, designed to enhance productivity when working with Ruby on Rails projects. The ERB snippets cover a wide range of common ERB patterns, including control structures, Rails helpers, and content management, making it easier to write clean and efficient ERB code.
More snippets will follow.

https://github.com/user-attachments/assets/51ec5af2-5e63-4bf1-a3d6-45e6bea0d10c


## Installation

To use these snippets in Zed Editor, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/gobijan/zed-rails-snippets.git
   ```

2. **Copy the Snippet File**:
   - Locate the `erb.json` file in the cloned repository.
   - Copy this file to Zed's snippet directory:
     ```bash
     cp erb.json ~/.config/zed/snippets/
     ```

3. **Reload Zed**:
   - Restart Zed or reload the snippets as per Zed's documentation to ensure the new snippets are loaded.

4. **Verify**:
   - Open an ERB file (`.erb` or `.html.erb`) in Zed.
   - Type `e` to see the list of available ERB snippets in the autocomplete menu.

## Usage

Once installed, these snippets can be triggered by typing their respective prefixes in an ERB file. For example, typing `ee` and pressing Tab will insert an ERB expression tag `<%= %>`.

### Snippet Categories

The snippets are organized into the following categories for easy reference:

- **Basic ERB**  
  - `ee`: Expression  
  - `er`: Statement  
  - `ec`: Comment  

- **Control Structures**  
  - `eif`: If Statement  
  - `eife`: If/Else Statement  
  - `eeach`: Each Loop  
  - `esafeeach`: Safe Each Loop  
  - `efor`: For Loop  
  - `eun`: Unless  

- **Rendering**  
  - `erp`: Render Partial  
  - `erpl`: Render Partial with Locals  
  - `erc`: Render Collection  

- **Helpers**  
  - `elt`: Link To  
  - `eit`: Image Tag  
  - `efw`: Form With  
  - `etf`: Text Field  
  - `eselect`: Select Tag  
  - `es`: Submit  
  - `ebt`: Button To  
  - `ect`: Content Tag  

- **Content Management**  
  - `ecf`: Content For  
  - `eyc`: Yield Content  
  - `ecfi`: Content For If  
  - `ecfd`: Content For With Default  

### Snippet Details

Below is a detailed list of all available snippets, including their prefixes, descriptions, and the code they generate:

- **ERB Expression**  
  - **Prefix**: `ee`  
  - **Description**: Inserts an ERB expression tag for outputting content  
  - **Code**: `<%= $1 %>`  

- **ERB Statement**  
  - **Prefix**: `er`  
  - **Description**: Inserts an ERB statement tag for Ruby code  
  - **Code**: `<% $1 %>`  

- **ERB Comment**  
  - **Prefix**: `ec`  
  - **Description**: Inserts an ERB comment  
  - **Code**: `<%# $1 %>`  

- **ERB If Statement**  
  - **Prefix**: `eif`  
  - **Description**: Inserts an ERB if statement  
  - **Code**:  
    ```erb
    <% if $1 %>
      $2
    <% end %>
    ```  

- **ERB If/Else Statement**  
  - **Prefix**: `eife`  
  - **Description**: Inserts an ERB if/else statement  
  - **Code**:  
    ```erb
    <% if $1 %>
      $2
    <% else %>
      $3
    <% end %>
    ```  

- **ERB Each Loop**  
  - **Prefix**: `eeach`  
  - **Description**: Inserts an ERB each loop for iterating over a collection  
  - **Code**:  
    ```erb
    <% $1.each do |$2| %>
      $3
    <% end %>
    ```  

- **ERB Safe Each Loop**  
  - **Prefix**: `esafeeach`  
  - **Description**: Inserts an ERB each loop with a presence check  
  - **Code**:  
    ```erb
    <% if $1.present? %>
      <% $1.each do |$2| %>
        $3
      <% end %>
    <% end %>
    ```  

- **ERB For Loop**  
  - **Prefix**: `efor`  
  - **Description**: Inserts an ERB for loop  
  - **Code**:  
    ```erb
    <% for $1 in $2 %>
      $3
    <% end %>
    ```  

- **ERB Render Partial**  
  - **Prefix**: `erp`  
  - **Description**: Renders a partial template  
  - **Code**: `<%= render partial: "$1" %>`  

- **ERB Render Partial with Locals**  
  - **Prefix**: `erpl`  
  - **Description**: Renders a partial with local variables  
  - **Code**: `<%= render partial: "$1", locals: { $2: $3 } %>`  

- **ERB Render Collection**  
  - **Prefix**: `erc`  
  - **Description**: Renders a partial for each item in a collection  
  - **Code**: `<%= render partial: "$1", collection: $2, as: :$3 %>`  

- **ERB Link To**  
  - **Prefix**: `elt`  
  - **Description**: Inserts a Rails link_to helper with optional class  
  - **Code**: `<%= link_to "$1", $2${3:, class: "$4"} %>`  

- **ERB Image Tag**  
  - **Prefix**: `eit`  
  - **Description**: Inserts a Rails image_tag helper with optional alt and class  
  - **Code**: `<%= image_tag "$1"${2:, alt: "$3", class: "$4"} %>`  

- **ERB Form With**  
  - **Prefix**: `efw`  
  - **Description**: Inserts a Rails form_with helper  
  - **Code**:  
    ```erb
    <%= form_with $1 do |f| %>
      $2
    <% end %>
    ```  

- **ERB Text Field**  
  - **Prefix**: `etf`  
  - **Description**: Inserts a Rails text_field helper with optional placeholder and class  
  - **Code**: `<%= f.text_field :$1${2:, placeholder: "$3", class: "$4"} %>`  

- **ERB Select Tag**  
  - **Prefix**: `eselect`  
  - **Description**: Inserts a Rails select helper with optional blank and class  
  - **Code**: `<%= f.select :$1, $2${3:, { include_blank: true }, { class: "$4" }} %>`  

- **ERB Submit**  
  - **Prefix**: `es`  
  - **Description**: Inserts a Rails submit button with optional class  
  - **Code**: `<%= f.submit "$1"${2:, class: "$3"} %>`  

- **ERB Button To**  
  - **Prefix**: `ebt`  
  - **Description**: Inserts a Rails button_to helper with optional class  
  - **Code**: `<%= button_to "$1", $2${3:, class: "$4"} %>`  

- **ERB Unless**  
  - **Prefix**: `eun`  
  - **Description**: Inserts an ERB unless statement  
  - **Code**:  
    ```erb
    <% unless $1 %>
      $2
    <% end %>
    ```  

- **ERB Content Tag**  
  - **Prefix**: `ect`  
  - **Description**: Inserts a Rails content_tag helper with optional class  
  - **Code**: `<%= content_tag :$1, "$2"${3:, class: "$4"} %>`  

- **ERB Content For**  
  - **Prefix**: `ecf`  
  - **Description**: Inserts a Rails content_for block  
  - **Code**:  
    ```erb
    <% content_for :$1 do %>
      $2
    <% end %>
    ```  

- **ERB Yield Content**  
  - **Prefix**: `eyc`  
  - **Description**: Yields content from a content_for block  
  - **Code**: `<%= yield :$1 %>`  

- **ERB Content For If**  
  - **Prefix**: `ecfi`  
  - **Description**: Conditionally yields content with a fallback  
  - **Code**:  
    ```erb
    <% if content_for?(:$1) %>
      <%= yield :$1 %>
    <% else %>
      $2
    <% end %>
    ```  

- **ERB Content For With Default**  
  - **Prefix**: `ecfd`  
  - **Description**: Yields content with a default value if absent  
  - **Code**: `<%= content_for?(:$1) ? yield(:$1) : "$2" %>`  

## Contributing

Contributions are welcome! If you have suggestions for new snippets or improvements to existing ones, please follow these steps:

1. **Fork the Repository**:
   - Click the "Fork" button on the repository page to create your own copy.

2. **Make Your Changes**:
   - Edit the `erb.json` file to add or modify snippets.
   - Ensure that all prefixes start with "e" and are unique.

3. **Submit a Pull Request**:
   - Push your changes to your forked repository.
   - Open a pull request with a clear description of your changes.

4. **Review and Merge**:
   - Your pull request will be reviewed, and if approved, merged into the main repository.

Thank you for contributing to making these snippets better for the community!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
