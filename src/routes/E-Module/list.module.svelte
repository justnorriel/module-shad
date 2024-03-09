<script lang="ts">
  import * as Tabs from "$lib/components/ui/tabs";
  import * as Table from "$lib/components/ui/table";
  import * as Select from "$lib/components/ui/select";
  import * as AlertDialog from "$lib/components/ui/alert-dialog";
  import { Button } from "$lib/components/ui/button";
  import PdfViewer from 'svelte-pdf';

  const subjects = [
    { value: "subject1", label: "Subject1" },
    { value: "subject2", label: "Subject2" },
    { value: "subject3", label: "Subject3" },
  ];

</script>


<div>
  <Tabs.Root value="account" class="w-auto sm:w-3/4 lg:w-3/4 mx-auto p-3 ">
    <Tabs.List class='grid grid-cols-2 items-center'>
      <Tabs.Trigger value="first-sem">1st sem</Tabs.Trigger>
      <Tabs.Trigger value="second-sem">2nd sem</Tabs.Trigger>
    </Tabs.List>

    <Tabs.Content value="first-sem">
      <Table.Root>
        <Table.Caption>A list of pdf module</Table.Caption>
        <Table.Header>
          <Table.Row>
            <Table.Head>
              <Select.Root>
                <Select.Trigger class="w-40">
                  <Select.Value placeholder="Select subject" />
                </Select.Trigger>
                <Select.Content>
                  <Select.Group>
                    <Select.Label>Subject</Select.Label>
                    {#each subjects as subject}
                    <Select.Item value={subject.value} label={subject.label}>
                      {subject.label}
                    </Select.Item>
                    {/each}
                  </Select.Group>
                </Select.Content>
                <Select.Input name="subject" />
              </Select.Root>
            </Table.Head>
            <Table.Head>Module #</Table.Head>
            <Table.Head>Title</Table.Head>
          </Table.Row>
        </Table.Header>
        <Table.Body>
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas01</Table.Cell>
            <Table.Cell>Introduction</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
          </Table.Row>
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas02</Table.Cell>
            <Table.Cell>Introduction</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
          </Table.Row>
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas03</Table.Cell>
            <Table.Cell>Introduction</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
          </Table.Row>
        </Table.Body>
      </Table.Root>
    </Tabs.Content>

    <Tabs.Content value="second-sem">
      <Table.Root>
        <Table.Caption>A list of pdf module</Table.Caption>
        <Table.Header>
          <Table.Row>
            <Table.Head>
              <Select.Root>
                <Select.Trigger class="w-40">
                  <Select.Value placeholder="Select subject" />
                </Select.Trigger>
                <Select.Content>
                  <Select.Group>
                    <Select.Label>Subject</Select.Label>
                    {#each subjects as subject}
                    <Select.Item value={subject.value} label={subject.label}>
                      {subject.label}
                    </Select.Item>
                    {/each}
                  </Select.Group>
                </Select.Content>
                <Select.Input name="favoriteFruit" />
              </Select.Root>
            </Table.Head>
            <Table.Head>Module #</Table.Head>
            <Table.Head>Title</Table.Head>
          </Table.Row>
        </Table.Header>
        <Table.Body>
          
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas01</Table.Cell>
            <Table.Cell>sas01</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
            </Table.Row>
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas02</Table.Cell>
            <Table.Cell>Introduction</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
          </Table.Row>
          <Table.Row>
            <Table.Cell>subj1</Table.Cell>
            <Table.Cell>sas03</Table.Cell>
            <Table.Cell>Introduction</Table.Cell>
            <Table.Cell> <AlertDialog.Root>
              <AlertDialog.Trigger asChild let:builder>
                  <Button builders={[builder]} variant="ghost" size="icon" class="flex font-normal gap-1">View</Button>
              </AlertDialog.Trigger>
              <AlertDialog.Content>
                  <AlertDialog.Header>
                      <AlertDialog.Title>About CITE e-module viewer</AlertDialog.Title>
                      <AlertDialog.Description class="font-center lg:w-full lg:h-full ">
                        <PdfViewer data={null} url='$lib/modules/ITE335-001-005.pdf'/>
                      </AlertDialog.Description>
                  </AlertDialog.Header>
                  <AlertDialog.Footer>
                      <AlertDialog.Action>Continue</AlertDialog.Action>
                  </AlertDialog.Footer>
              </AlertDialog.Content>
          </AlertDialog.Root></Table.Cell>
          </Table.Row>
        </Table.Body>
      </Table.Root>
    </Tabs.Content>
  </Tabs.Root>
</div>